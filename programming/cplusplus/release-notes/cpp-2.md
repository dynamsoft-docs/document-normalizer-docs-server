---
layout: default-layout
title: Release Notes for C++ Edition - v2.x
description: This is the release notes page of Dynamsoft Document Normalizer SDK C++ Edition for version 2.x.
keywords: release notes, c++, 
needGenerateH3Content: false
permalink: /programming/cplusplus/release-notes/cpp-2.html
---

# Release Notes for C++ Edition - v2.x

## 2.0.20 (10/26/2023)

### New

* Added the following preset templates:
  * PT_READ_BARCODES_SPEED_FIRST
  * PT_READ_BARCODES_READ_RATE_FIRST
  * PT_READ_BARCODES_BALANCED
  * PT_READ_SINGLE_BARCODE
  * PT_READ_DENSE_BARCODES
  * PT_READ_DISTANT__BARCODES
  * PT_RECOGNIZE_NUMBERS
  * PT_RECOGNIZE_LETTERS
  * PT_RECOGNIZE_NUMBERS_AND_LETTERS
  * PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS
  * PT_RECOGNIZE_UPPERCASE_LETTERS
* Added parameter `Page` to `ImageSource` object.
* Added a new method `SetPages` to the class `CDirectoryFetcher` and class `CFileFetcher`.
* Added `CImageSourceErrorListener` to receive the errors from an image source. 
* Added method `SetErrorListener` to class `CImageSourceAdapter` to add the `CImageSourceErrorListener`.
* Added a new parameter `minImageCaptureInterval` which can be set via the struct `SimplifiedCaptureVisionSettings` or the `CaptureVisionTemplate` object of a JSON template file.
* Added "UNKNOWN" as a supported value of the `TextDetectionMode.Direction` parameter. Changed the default value of `Direction` to "UNKNOWN".
* Added the following error codes:
  * EC_FILE_ALREADY_EXISTS
  * EC_CREATE_FILE_FAILED
  * EC_IMGAE_DATA_INVALID

### Improved

* The class `CDirectoryFetcher` and `CFileFetcher` will be able to return error codes via `CImageSourceErrorListener`
* Updated the error codes of the method `SaveToFile` of the class `CImageManager`.
* Optimize the logic to support calling `CIntermediateResultManager.AddResultReceiver` and  `CIntermediateResultManager.RemoveResultReceiver` after StartCapturing.
* Added ability to output all templates via methods `OutputSettings` and `OutputSettingsToFile` by specifying "*" for the parameter `templateName`.

### Fixed

* Small fixes and tweaks.

### Changed

* Changed the upper limit to the `DuplicateForgetTime`, which is 3 minutes.
* Changed the timing of `OnOriginalImageResultReceived` so that it is triggered immediately after receiving the image.
* Changed the constructors of the following classes from public to protected.
  * CImageTag
  * CCapturedResultReceiver
  * CCapturedResultFilter
  * CImageSourceAdapter
  * CProactiveImageSourceAdapter
  * CIntermediateResultUnit
  * CIntermediateResultReceiver
* Remove const modifiers of all callback methods of class `CCapturedResultReceiver` and class `CIntermediateResultReceiver`.

## 2.0.10(08/08/2023)

### Fixed

* Fixed crash bugs that happen in rare cases.

* Fixed a bug where the local license is not successfully updated in some case.

### Improved

* Improved the implementation of the StopCapturing method to prevent deadlock when invoked in the management thread.

### New

* Added a new class `CVector4` in the core module.

* Added new methods `SetTransformMatrix` and `GetTransformMatrix` to the class `CIntermediateResultUnit`. Enumeration `TransformMatrixType` is also added to support users specifying the type of the target matrix.

* Added enumeration `RasterDataSource` to specify the raster data source when reading PDF files. The previous enumeration `TargetType` is removed. The attribute `TargetType type` of Class `CPDFReadingParameter` is replaced by `RasterDataSource rasterDataSource`.  

* Added `CRIT_NORMALIZED_IMAGE` to the available result types of result cross-verification.

* Added method `GetContours` to the class `CContourUnit` to get all the `CContour` objects contained in the unit and their hierarchies.

### Changed

* Changed the parameters and the return value of the method `GetLongLine` of CLongLinesUnit class. The method will require an `index` value as the parameter and return a `CLineSegment` object as the return value.

* Changed the structure of class `CPoint`.

* Renamed method `GetRawImage` to `GetOriginalImage`.

* Renamed method `GetSourceImageHashId` to `GetOriginalImageHashId`. This change applies to the following classes:

  * `CIntermediateResultUnit`

  * `CCapturedResult`

  * `CDecodedBarcodesResult`

  * `CRecognizedTextLinesResult`

  * `CNormalizedImagesResult`

  * `CDetectedQuadsResult`

  * `CParsedResult`

* Renamed method `GetSourceImageTag` to `GetOriginalImageTag`. This change applies to the following classes:

  * `CIntermediateResultUnit`

  * `CCapturedResult`

  * `CDecodedBarcodesResult`

  * `CRecognizedTextLinesResult`

  * `CNormalizedImagesResult`

  * `CDetectedQuadsResult`

  * `CParsedResult`

* Renamed methods `GetCount` to `GetItemsCount`. This change applies to the following classes:

  * `CCapturedResult`

  * `CDecodedBarcodesResult`

  * `CRecognizedTextLinesResult`

  * `CNormalizedImagesResult`

  * `CDetectedQuadsResult`

  * `CParsedResult`

* Renamed an enumeration member of `CapturedResultItemType` from `CRIT_RAW_IMAGE` to `CRIT_ORIGINAL_IMAGE`.

* Renamed a method of `CapturedResultReceiver` from `OnRawImageResultReceived` to `OnOriginalImageResultReceived`.

* Renamed a method of `CapturedResultFilter` from `OnRawImageResultReceived` to `OnOriginalImageResultReceived`.

* Renamed the class `CRawImageResultItem` to `COriginalImageResultItem`.

* Renamed an enumeration member of `BufferOverflowProtectionMode` from `BOPM_APPEND` to `BOPM_UPDATE`.

* The following methods are renamed:

  * Renamed `EnableResultVerification` to `EnableResultCrossVerification`.

  * Renamed `isResultVerificationEnable` to `isResultCrossVerificationEnabled`.

  * Renamed `EnableDuplicateFilter` to `EnableResultDeduplication`.

  * Renamed `isDuplicateFilterEnabled` to `isResultDeduplicationEnabled`.

* Renamed parameter `CornerAngleRangeArray` to `CornerAngleRange`. The range of the sub parameter `MinValue` is restricted to [0,90] and the range of `MaxValue` is restricted to [90,180].

### Removed

* Removed methods `SetLocalToSourceImageTransformMatrix` and `GetLocalToSourceImageTransformMatrix` from class `CIntermediateResultUnit`.

* Removed methods `SetRotationTransformMatrix` and `GetRotationTransformMatrix` from class `CIntermediateResultUnit`.

* Removed methods `GetCount` and `GetContour` from class `CContourUnit`. Use the method `GetContours` instead.

## 2.0.0 (07/04/2023)

### Highlights

{%- include release-notes/product-highlight-2.0.0.md -%}
