---
layout: default-layout
title: Dynamsoft Document Normalizer C++ API Reference - Main Page
description: This is the main page of Dynamsoft Document Normalizer SDK API Reference for C++ Language.
keywords: CDocumentNormalizer, api reference, C++
permalink: /programming/cplusplus/api-reference/index-v2.0.0.html
---

# API Reference - C++

## Primary Class

- [`CCaptureVisionRouter`]({{ site.dcv_cpp_api }}capture-vision-router/capture-vision-router.html)

## Input

- [`CDirectoryFetcher`]({{ site.dcv_cpp_api }}utility/directory-fetcher.html)
- [`CFileFetcher`]({{ site.dcv_cpp_api }}utility/file-fetcher.html)
- [`CImageSourceAdapter`]({{ site.dcv_cpp_api }}core/basic-structures/image-source-adapter.html)
- [`CProactiveImageSourceAdapter`]({{ site.dcv_cpp_api }}utility/proactive-image-source-adapter.html)

## Final Results

- [`CCapturedResultReceiver`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-receiver.html)
- [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html)
- [`CCapturedResult`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result.html)
- [`CDetectedQuadResultItem`]({{ site.ddn_cpp_api }}detected-quad-result-item.html)
- [`CDetectedQuadsResult`]({{ site.ddn_cpp_api }}detected-quads-result.html)
- [`CNormalizedImageResultItem`]({{ site.ddn_cpp_api }}normalized-image-result-item.html)
- [`CNormalizedImagesResult`]({{ site.ddn_cpp_api }}normalized-images-result.html)
- [`CRawImageResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/raw-image-result-item.html)

## Final Results Filters

- [`CCapturedResultFilter`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-filter.html)
- [`CMultiFrameResultCrossFilter`]({{ site.dcv_cpp_api }}utility/multi-frame-result-cross-filter.html)

## Intermediate Results

- [`CIntermediateResultManager`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-manager.html)
- [`CIntermediateResultReceiver`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`CObservationParameters`]({{ site.dcv_cpp_api }}core/intermediate-results/observed-parameters.html)
- [`IntermediateResultExtraInfo`]({{ site.dcv_cpp_api }}core/structs/intermediate-result-extra-info.html)
- [`CIntermediateResult`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result.html)
- [`CIntermediateResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html)
- [`CPredetectedRegionsUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-regions-unit.html)
- [`CDetectedQuadsUnit`]({{ site.ddn_cpp_api }}detected-quads-unit.html)
- [`CNormalizedImagesUnit`]({{ site.ddn_cpp_api }}normalized-image-unit.html)
- [`CRegionObjectElement`]({{ site.dcv_cpp_api }}core/intermediate-results/region-object-element.html)
- [`CPredetectedRegionElement`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-region-element.html)
- [`CDetectedQuadElement`]({{ site.ddn_cpp_api }}detected-quad-element.html)
- [`CNormalizedImageElement`]({{ site.ddn_cpp_api }}normalized-image-element.html)
- [`CBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/binary-image-unit.html)
- [`CCandidateQuadEdgesUnit`]({{ site.ddn_cpp_api }}candidate-quad-edges-unit.html)
- [`CColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/colour-image-unit.html)
- [`CContoursUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/contours-unit.html)
- [`CCornersUnit`]({{ site.ddn_cpp_api }}corners-unit.html)
- [`CEnhancedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`CGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/grayscale-image-unit.html)
- [`CLineSegmentsUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/line-segments-unit.html)
- [`CLongLinesUnit`]({{ site.ddn_cpp_api }}long-lines-unit.html)
- [`CScaledDownColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`CTextRemovedBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/text-removed-binary-image-unit.html)
- [`CTextZonesUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/text-zones-unit.html)
- [`CTextureDetectionResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`CTextureRemovedBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`CTextureRemovedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`CTransformedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

## Settings

- [`SimplifiedCaptureVisionSettings`]({{ site.dcv_cpp_api }}capture-vision-router/structs/simplified-capture-vision-settings.html)
- [`CPresetTemplate`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/preset-template.html)

## State Listener

- [`CCaptureStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CImageSourceStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## [`CLicenseManager`]({{ site.dcv_cpp_api }}license/license-manager.html)

## Basic Structure

- [`CContour`]({{ site.dcv_cpp_api }}core/basic-structures/contour.html)
- [`CCorner`]({{ site.dcv_cpp_api }}core/basic-structures/corner.html)
- [`CEdge`]({{ site.dcv_cpp_api }}core/basic-structures/edge.html)
- [`CFileImageTag`]({{ site.dcv_cpp_api }}core/basic-structures/file-image-tag.html)
- [`CImageData`]({{ site.dcv_cpp_api }}core/basic-structures/image-data.html)
- [`CImageTag`]({{ site.dcv_cpp_api }}core/basic-structures/image-tag.html)
- [`CLineSegment`]({{ site.dcv_cpp_api }}core/basic-structures/line-segment.html)
- [`CPDFReadingParameter`]({{ site.dcv_cpp_api }}core/basic-structures/pdf-reading-parameter.html)
- [`CPoint`]({{ site.dcv_cpp_api }}core/basic-structures/point.html)
- [`CQuadrilateral`]({{ site.dcv_cpp_api }}core/basic-structures/quadrilateral.html)
- [`CRect`]({{ site.dcv_cpp_api }}core/basic-structures/rect.html)
- [`CVideoFrameTag`]({{ site.dcv_cpp_api }}core/basic-structures/video-frame-tag.html)

## Modules

- [`CCaptureVisionRouterModule`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CDocumentNormalizerModule`]({{ site.ddn_cpp_api }}document-normalizer-module.html)
- [`CCoreModule`]({{ site.dcv_cpp_api }}core/basic-structures/core-module.html)
- [`CLicenseModule`]({{ site.dcv_cpp_api }}license/license-module.html)
- [`CUtilityModule`]({{ site.dcv_cpp_api }}utility/utility-module.html)
- [`CImageProcessingModule`]({{ site.dcv_cpp_api }}image-processing/image-processing-module.html)

## Enumerations

- [`BufferOverflowProtectionMode`]({{ site.dcv_enumerations }}core/buffer-overflow-protection-mode.html?src=cpp&&lang=cpp)
- [`CapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)
- [`CornerType`]({{ site.dcv_enumerations }}core/corner-type.html?src=cpp&&lang=cpp)
- [`ErrorCode`]({{ site.dcv_enumerations }}core/error-code.html?src=cpp&&lang=cpp)
- [`GrayscaleTransformationMode`]({{ site.dcv_enumerations }}core/grayscale-transformation-mode.html?src=cpp&&lang=cpp)
- [`ImageCaptureDistanceMode`]({{ site.dcv_enumerations }}core/image-capture-distance-mode.html?src=cpp&&lang=cpp)
- [`ImagePixelFormat`]({{ site.dcv_enumerations }}core/image-pixel-format.html?src=cpp&&lang=cpp)
- [`ImageSourceState`]({{ site.dcv_enumerations }}capture-vision-router/image-source-state.html?src=cpp&&lang=cpp)
- [`ImageTagType`]({{ site.dcv_enumerations }}core/image-tag-type.html?src=cpp&&lang=cpp)
- [`IntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?src=cpp&&lang=cpp)
- [`PDFReadingMode`]({{ site.dcv_enumerations }}core/pdf-reading-mode.html?src=cpp&&lang=cpp)
- [`RegionObjectElementType`]({{ site.dcv_enumerations }}core/region-object-element-type.html?src=cpp&&lang=cpp)
- [`SectionType`]({{ site.dcv_enumerations }}core/section-type.html?src=cpp&&lang=cpp)
- [`TargetType`]({{ site.dcv_enumerations }}core/target-type.html?src=cpp&&lang=cpp)
- [`VideoFrameQuality`]({{ site.dcv_enumerations }}core/video-frame-quality.html?src=cpp&&lang=cpp)
- [`ColourChannelUsageType`]({{ site.enumerations}}core/colour-channel-usage-type.html?src=cpp&&lang=cpp)
