---
layout: default-layout
title: Release Notes for C++ Edition - v2.x
description: This is the release notes page of Dynamsoft Document Normalizer SDK C++ Edition for version 2.x.
keywords: release notes, c++, 
needGenerateH3Content: false
permalink: /programming/cplusplus/release-notes/cpp-2.html
---

# Release Notes for C++ Edition - v2.x

## 2.4.10 (07/23/2024)

### New

- Added a new parameter [`MinQuadrilateralAreaRatio`]({{ site.dcv_parameters_reference }}document-normalizer-task-settings/quadrilateral-detection-modes.html) to define the minimum targeting document area. The parameter is available via both the parameter template and the [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_cpp_api }}simplified-document-normalizer-settings.html).
- Added a new parameter [`ExpectedDocumentsCount`]({{ site.dcv_parameters_reference }}document-normalizer-task-settings/expected-documents-count.html) to define the expected document count for detection. The parameter is available via both the parameter template and the [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_cpp_api }}simplified-document-normalizer-settings.html).
- Added a new function [`Clone`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html#clone) to the class [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html).
- Added a new function [`AddItem`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html#additem) to the class [`CCapturedResult`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html).
- Add a new charge way, `TimeSliceCount`.

### Changed

- Changed the maximum length of the `DeviceFriendlyName` to 255. If the length exceeds 255, it will be truncated.

### Fixed

- Fixed a bug where `CaptureVisionRouter.StartCapturing` would erroneously halt the fetching process when its status was running, leading to an unnecessary stop and restart of the fetching operation.
- Fixed a bug where `CDirectoryFetcher` would prematurely read an image before verifying if the buffer was full, resulting in potential loss of the image that did not make it into the buffer upon calling `StopFetching`.

## 2.2.10 (03/01/2024)

### Improved

- Security update for `DynamsoftDocumentNormalizer` library and other corresponding libraries.
- Supported multiple instances of the class [`CCaptureVisionRouter`]({{ site.dcv_cpp_api }}capture-vision-router/capture-vision-router.html).
- Improved the usage count logic of the concurrent license mode.
- Improved the experience of local cache usage when failing to connect the license server. The renewal of the local cache is optimized as well.

### New

- Added new error codes:
  - `EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE`
  - `EC_LICENSE_CACHE_USED`
- Added a virtual destructor to the interface [`CImageSourceErrorListener`]({{ site.dcv_cpp_api }}core/basic-structures/image-source-error-listener.html) to prevent memory leaks.
- Added a new function [`GetDetectedQuadsResult`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html#getdetectedquadsresult) to the `CCapturedResult` class to get all the result items with the type `CRIT_DETECTED_QUAD`.
- Added a new function [`GetNormalizedImagesResult`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html#getnormalizedimagesresult) to the `CCapturedResult` class to get all the result items with the type `CRIT_NORMALIZED_IMAGE`.
- Added new virtual destructors to the following interfaces to prevent memory leaks.
  - [`CCaptureStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
  - [`CImageSourceStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

### Changed

- Changed the internal logic of the function [`SetResultUnitTypesOnlyForInput`]({{ site.dcv_cpp_api }}core/intermediate-results/observed-parameters.html#setresultunittypesonlyforinput) of `ObservationParameters`. The function only takes effect when the callback of the specified result unit is implemented.

### Fixed

- Fixed a crash bug of the Replace method of the [`IntermediateResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) class. The method will return the error code `EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE` when the result type is mismatched.
- Fixed a bug where error messages are not output when parsing the parameter templates.
- Fixed a bug where the capture might be blocked due to the network latency.
- Fixed a bug where the `DetectAndNormalizeDocument` task might be approved without a valid license.
- Fixed the bugs of usage count.
  - Count twice for a single PDF417 barcode when a code parser task is implemented on the result.
  - The barcode decoding result might not be uploaded timely.
  - The usage count of text line recognition might be double counted when the intermediate results are output.
  - The document boundary detection result might be miscounted.
  - Patchcode might be counted even if there is no Patchcode license item.

## 2.2.0 (01/16/2024)

### Highlights

- Introduced the capability for users to influence the image processing process by altering intermediate results. Users can now clone, edit, and substitute intermediate result units within the callback function of each type. Subsequent operations will then proceed based on the updated unit.
- Introduced a feature for multi-condition filtering across products. Users can now specify filtering criteria for the task results of a `TargetROIDef` by implementing an `OutputTaskSetting` based on the task results of varying products from descendant `TargetROIDef` objects.
- Enhanced the `Offset` parameter in `TargetROIDef`. Users now have the capability to meticulously customize components of the coordinate system, including the origin, X-axis, and Y-axis, for precise offset calculation.

### Changelogs

#### New

- Updated the template system
  - Added `StringLengthRange` for `TextDetectionMode`.
  - Added `ReferenceTaskNameArray` under `Location.ReferenceObjectFilter` to filter the reference objects generated by the task name.
  - Added the support of the `OutputTaskSetting` definition. The following subparameters are available in `OutputTaskSetting` object:
    - `OutputCondition`
    - `TaskResultArray`
    - `TargetROIDefName`
    - `TaskSettingNameArray`
    - `BackwardReferenceOutput`
    - `ReferenceTaskNameArray`
    - `ReferenceResultTypeArray`
    - `Operator`
  - Offset parameter is optimized.
    - Added `ReferenceObjectType` to specify whether the reference object is an atomic object or the whole image.
    - Added `ReferenceXAxis` & `ReferenceYAxis` to define the X & Y axis.
    - Modified `FirstPoint`, `SecondPoint`, `ThirdPoint` & `FourthPoint`. You can specify whether the X or Y coordinate of the point is measured by percentage.
    - Deprecated `ReferenceObjectSize` Type.
- The following classes are migrated from `DynamsoftCore` module to the `DynamsoftCaptureVisionRouter` module:
  - `CIntermediateResultReceiver`
  - `CapturedResultReceiver`
  - `CapturedResultFilter`
  - `CIntermediateResultManager`
- Added a new class back method `OnShortLinesUnitReceived` to the `CIntermediateResultReceiver` class.
- Added a new class `CAbstractIntermediateResultReceiver`. It is the super class of the `CIntermediateResultReceiver`.
- Added methods `PauseCapturing` and `ResumeCapturing`. Two new `CapturedState` members, `CS_PAUSED` and `CS_RESUMED`, are added as well.
- Added a new property `documentSettings` to struct `SimplifiedCaptureVisionSettings`. The corresponding struct `SimplifiedDocumentNormalizerSettings` is added to the `DynamsoftDocumentNormalizer` module to store the `documentSettings`.
- Added the following methods to the `CObservationParameters` class to specify the `input only` result unit.
  - `SetResultUnitTypesOnlyForInput`
  - `GetResultUnitTypesOnlyForInput`
  - `IsResultUnitTypeOnlyForInput`
- Added the following methods to the `CRegionObjectElement` class to support the intermediate result modification.
  - `SetLocation`
  - `Clone`
  - `Retain`
  - `Release`
- Added a new method `Replace` to the `CIntermediateResultUnit` class to support the replacement of intermediate result units.
- Added `SetImageData` methods to the following classes:
  - `CColourImageUnit`
  - `CScaledDownColourImageUnit`
  - `CGrayscaleImageUnit`
  - `CTransformedGrayscaleImageUnit`
  - `CEnhancedGrayscaleImageUnit`
  - `CBinaryImageUnit`
  - `CTextureRemovedGrayscaleImageUnit`
  - `CTextureRemovedBinaryImageUnit`
  - `CTextRemovedBinaryImageUnit`
- Added new methods to the `CPredetectedRegionsUnit` class to add, remove or set the predetected regions.
- Added new methods to the `CLineSegmentsUnit` class to add, remove or set the line segments.
- Added new methods to the `CTextZonesUnit` class to add, remove or set the text zones. Added a new class `CTextZone` to store the information of a single text zone.
- Added a new method `SetContours` to the `CContourUnit` class.
- Added new methods to the `CTextureDetectionResultUnit` class to set the X & Y spacing.
- Added a new intermediate result unit, `CShortLinesUnit`, to output the detected short lines. The corresponding enumeration member `IRUT_SHORT_LINES` is added to the `IntermediateResultUnitType`.
- Added the following methods to the `CCapturedResultItem` class
  - `GetTargetROIDefName`
  - `GetTaskName`
  - `Retain`
  - `Release`
- Added the following new error codes
  - `EC_IMAGE_SIZE_NOT_MATCH`
  - `EC_IMAGE_PIXEL_FORMAT_NOT_MATCH`
  - `EC_SECTION_LEVEL_RESULT_IRREPLACEABLE`
  - `EC_AXIS_DEFINITION_INCORRECT`
  - `EC_TEXT_LINE_GROUP_LAYOUT_CONFLICT`
  - `EC_TEXT_LINE_GROUP_REGEX_CONFLICT`
- Added the following methods to the `CCapturedResult` class.
  - A new override constructor.
  - `Retain`
  - `Release`
- Updated `CImageData` class
  - Change the return value of `GetBytesLength` from int to unsigned long long.
  - Added a new constructor.
- Added a new supported image pixel format, binary 8 inverted. The corresponding enumeration member is added to the `ImagePixelFormat`.
- Added return value for the `Retain` method of the `CIntermediateResultUnit` class. The method will return the pointer of the current `CIntermediateResultUnit`.
- Added new methods to the `CLongLinesUnit` class to add, set or remove the line segments of the unit.
- Added new methods to the `CCornersUnit` class to add, set or remove the corners of the unit.
- Added new methods to the `CCandidateQuadEdgesUnit` class to add, set or remove the candidate quad edges of the unit.
- Added new methods to the `CDetectedQuadsUnit` class to add, set or remove the detected quad elements of the unit.
- Added new methods to the `CNormalizedImagesUnit` class to set or remove the normalized image element of the unit.
- Added the following methods to the `CNormalizedImagesResult` class.
  - A new constructor
  - `Retain`
  - `Release`
- Added the following methods to the `CDetectedQuadsResult` class.
  - A new constructor
  - `Retain`
  - `Release`
- Added `SimplifiedDocumentNormalizerSettings`  struct to configure basic settings of document processing.
- Added the following methods to the `CDocumentNormalizerModule` class to create the corresponding elements:
  - `CreateNormalizedImageElement`
  - `CreateDetectedQuadElement`
- Added a new enumeration `ImageColourMode` to specify the colour mode of the normalized image.
- Added a new method `CreatePredetectedRegionElement` to the `CImageProcessingModule` class to create the predetected region element.

#### Fixed

- Fixed a bug where the internal table boundaries were recognized as the document boundaries.
- Fixed a crash bug that might happen when triggering the `SetNextImageToReturn` method of the `ImageSourceAdapter` class.

#### Break Changes

- Changed the logic of the `StopCapturing` method.
  - `CaptureResultReceiver` will not receive results after `StopCapturing` is triggered with `waitForRemainingTasks` false.
  - Support stop capturing after the `PauseCapturing` method is triggered.
- Changed the logic of the `capturedResultItemTypes` setting of `SimplifiedCaptureVisionSettings`:
  - If the result item types don't match the specified template, the method UpdateSettings will return the error code `EC_PARAMETER_VALUE_INVALID` with the message "The captured result item types do not match the task configurations in the template".
  - Based on the `capturedResultItemTypes` setting, the irrelevant tasks will be removed from the template.
  - The `capturedResultItemTypes` should include at least one of the `CRIT_BARCODE`, `CRIT_TEXT_LINE`, `CRIT_DETECTED_QUAD`, `CRIT_NORMALIZED_IMAGE`. Otherwise, the method `UpdateSettings` will return the error code `EC_PARAMETER_VALUE_INVALID` with the message " The captured result item types should contain at least one task result type ".
- Refactored the `CContour` class. Please view API reference - `CContour` class for more information.
- The destructor functions of the following classes are changed to protected:
  - `CCandidateQuadEdgesUnit`
  - `CCornersUnit`
  - `CDetectedQuadElement`
  - `CDetectedQuadsUnit`
  - `CLongLinesUnit`
  - `CNormalizedImageElement`
  - `CNormalizedImageUnit`
  - `CNormalizedImagesResult`
  - `CDetectedQuadsResult`
- Change the compiler option of the runtime library of Windows DLLs from MD to MT.
- The `DeepNeuralNetwork` module is separated from the `DynamsoftImageProcessing` module.

## 2.0.20 (10/26/2023)

### New

- Added the following preset templates:
  - PT_READ_BARCODES_SPEED_FIRST
  - PT_READ_BARCODES_READ_RATE_FIRST
  - PT_READ_BARCODES_BALANCED
  - PT_READ_SINGLE_BARCODE
  - PT_READ_DENSE_BARCODES
  - PT_READ_DISTANT__BARCODES
  - PT_RECOGNIZE_NUMBERS
  - PT_RECOGNIZE_LETTERS
  - PT_RECOGNIZE_NUMBERS_AND_LETTERS
  - PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS
  - PT_RECOGNIZE_UPPERCASE_LETTERS
- Added parameter `Page` to `ImageSource` object.
- Added a new method `SetPages` to the class `CDirectoryFetcher` and class `CFileFetcher`.
- Added `CImageSourceErrorListener` to receive the errors from an image source. 
- Added method `SetErrorListener` to class `CImageSourceAdapter` to add the `CImageSourceErrorListener`.
- Added a new parameter `minImageCaptureInterval` which can be set via the struct `SimplifiedCaptureVisionSettings` or the `CaptureVisionTemplate` object of a JSON template file.
- Added "UNKNOWN" as a supported value of the `TextDetectionMode.Direction` parameter. Changed the default value of `Direction` to "UNKNOWN".
- Added the following error codes:
  - EC_FILE_ALREADY_EXISTS
  - EC_CREATE_FILE_FAILED
  - EC_IMGAE_DATA_INVALID

### Improved

- The class `CDirectoryFetcher` and `CFileFetcher` will be able to return error codes via `CImageSourceErrorListener`
- Updated the error codes of the method `SaveToFile` of the class `CImageManager`.
- Optimize the logic to support calling `CIntermediateResultManager.AddResultReceiver` and  `CIntermediateResultManager.RemoveResultReceiver` after StartCapturing.
- Added ability to output all templates via methods `OutputSettings` and `OutputSettingsToFile` by specifying "*" for the parameter `templateName`.

### Fixed

- Small fixes and tweaks.

### Changed

- Changed the upper limit to the `DuplicateForgetTime`, which is 3 minutes.
- Changed the timing of `OnOriginalImageResultReceived` so that it is triggered immediately after receiving the image.
- Changed the constructors of the following classes from public to protected.
  - CImageTag
  - CCapturedResultReceiver
  - CCapturedResultFilter
  - CImageSourceAdapter
  - CProactiveImageSourceAdapter
  - CIntermediateResultUnit
  - CIntermediateResultReceiver
- Remove const modifiers of all callback methods of class `CCapturedResultReceiver` and class `CIntermediateResultReceiver`.

## 2.0.10(08/08/2023)

### Fixed

- Fixed crash bugs that happen in rare cases.

- Fixed a bug where the local license is not successfully updated in some case.

### Improved

- Improved the implementation of the StopCapturing method to prevent deadlock when invoked in the management thread.

### New

- Added a new class `CVector4` in the core module.

- Added new methods `SetTransformMatrix` and `GetTransformMatrix` to the class `CIntermediateResultUnit`. Enumeration `TransformMatrixType` is also added to support users specifying the type of the target matrix.

- Added enumeration `RasterDataSource` to specify the raster data source when reading PDF files. The previous enumeration `TargetType` is removed. The attribute `TargetType type` of Class `CPDFReadingParameter` is replaced by `RasterDataSource rasterDataSource`.  

- Added `CRIT_NORMALIZED_IMAGE` to the available result types of result cross-verification.

- Added method `GetContours` to the class `CContourUnit` to get all the `CContour` objects contained in the unit and their hierarchies.

### Changed

- Changed the parameters and the return value of the method `GetLongLine` of CLongLinesUnit class. The method will require an `index` value as the parameter and return a `CLineSegment` object as the return value.

- Changed the structure of class `CPoint`.

- Renamed method `GetRawImage` to `GetOriginalImage`.

- Renamed method `GetSourceImageHashId` to `GetOriginalImageHashId`. This change applies to the following classes:

  - `CIntermediateResultUnit`

  - `CCapturedResult`

  - `CDecodedBarcodesResult`

  - `CRecognizedTextLinesResult`

  - `CNormalizedImagesResult`

  - `CDetectedQuadsResult`

  - `CParsedResult`

- Renamed method `GetSourceImageTag` to `GetOriginalImageTag`. This change applies to the following classes:

  - `CIntermediateResultUnit`

  - `CCapturedResult`

  - `CDecodedBarcodesResult`

  - `CRecognizedTextLinesResult`

  - `CNormalizedImagesResult`

  - `CDetectedQuadsResult`

  - `CParsedResult`

- Renamed methods `GetCount` to `GetItemsCount`. This change applies to the following classes:

  - `CCapturedResult`

  - `CDecodedBarcodesResult`

  - `CRecognizedTextLinesResult`

  - `CNormalizedImagesResult`

  - `CDetectedQuadsResult`

  - `CParsedResult`

- Renamed an enumeration member of `CapturedResultItemType` from `CRIT_RAW_IMAGE` to `CRIT_ORIGINAL_IMAGE`.

- Renamed a method of `CapturedResultReceiver` from `OnRawImageResultReceived` to `OnOriginalImageResultReceived`.

- Renamed a method of `CapturedResultFilter` from `OnRawImageResultReceived` to `OnOriginalImageResultReceived`.

- Renamed the class `CRawImageResultItem` to `COriginalImageResultItem`.

- Renamed an enumeration member of `BufferOverflowProtectionMode` from `BOPM_APPEND` to `BOPM_UPDATE`.

- The following methods are renamed:

  - Renamed `EnableResultVerification` to `EnableResultCrossVerification`.

  - Renamed `isResultVerificationEnable` to `isResultCrossVerificationEnabled`.

  - Renamed `EnableDuplicateFilter` to `EnableResultDeduplication`.

  - Renamed `isDuplicateFilterEnabled` to `isResultDeduplicationEnabled`.

- Renamed parameter `CornerAngleRangeArray` to `CornerAngleRange`. The range of the sub parameter `MinValue` is restricted to [0,90] and the range of `MaxValue` is restricted to [90,180].

### Removed

- Removed methods `SetLocalToSourceImageTransformMatrix` and `GetLocalToSourceImageTransformMatrix` from class `CIntermediateResultUnit`.

- Removed methods `SetRotationTransformMatrix` and `GetRotationTransformMatrix` from class `CIntermediateResultUnit`.

- Removed methods `GetCount` and `GetContour` from class `CContourUnit`. Use the method `GetContours` instead.

## 2.0.0 (07/04/2023)

### Highlights

{%- include release-notes/product-highlight-2.0.0.md -%}
