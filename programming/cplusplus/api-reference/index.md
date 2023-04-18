---
layout: default-layout
title: Dynamsoft Document Normalizer C++ API Reference - Main Page
description: This is the main page of Dynamsoft Document Normalizer SDK API Reference for C++ Language.
keywords: CDocumentNormalizer, api reference, C++
permalink: /programming/cplusplus/api-reference/index.html
---

# API Reference - C++

## Primary Class

- [`CCaptureVisionRouter`]({{ site.dcv_cpp_api }}capture-vision-router/capture-vision-router.html)

## Input

- [`CDirectoryFetcher`]({{ site.dcv_cpp_api }}utility/directory-fetcher.html)
- [`CImageSourceAdapter`]({{ site.dcv_cpp_api }}core/basic-structures/image-source-adapter.html)
- [`CProactiveImageSourceAdapter`]({{ site.dcv_cpp_api }}utility/proactive-image-source-adapter.html)

## Final Results

- [`CCapturedResultReceiver`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)
- [`CCapturedResult`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result.html)
- [`CCapturedResultArray`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-array.html)
- [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html)
- [`CDetectedQuadResultItem`]({{ site.cpp_api }}detected-quad-result-item.html)
- [`CDetectedQuadsResult`]({{ site.cpp_api }}detected-quads-result.html)
- [`CNormalizedImageResultItem`]({{ site.cpp_api }}normalized-image-result-item.html)
- [`CNormalizedImagesResult`]({{ site.cpp_api }}normalized-images-result.html)
- [`CRawImageResultItem`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/raw-image-result-item.html)

## Intermediate Results

- [`CIntermediateResultReceiver`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`CBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/binary-image-unit.html)
- [`CColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/colour-image-unit.html)
- [`CContoursUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/contours-unit.html)
- [`CEnhancedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`CGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/grayscale-image-unit.html)
- [`CIntermediateResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html)
- [`CLineSegmentsUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/line-segments-unit.html)
- [`CPredetectedRegionElement`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-region-element.html)
- [`CPredetectedRegionsUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-regions-unit.html)
- [`CRegionObjectElement`]({{ site.dcv_cpp_api }}core/intermediate-results/region-object-element.html)
- [`CScaledDownColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`CTextRemovedBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/text-removed-binary-image-unit.html)
- [`CTextZonesUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/text-zones-unit.html)
- [`CTextureDetectionResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`CTextureRemovedBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`CTextureRemovedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`CTransformedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/transformed-grayscale-image-unit.html)
- [`CCandidateQuadEdgesUnit`]({{ site.cpp_api }}candidate-quad-edges-unit.html)
- [`CCornersUnit`]({{ site.cpp_api }}corners-unit.html)
- [`CDetectedQuadElement`]({{ site.cpp_api }}detected-quad-element.html)
- [`CDetectedQuadsUnit`]({{ site.cpp_api }}detected-quads-unit.html)
- [`CLongLinesUnit`]({{ site.cpp_api }}long-lines-unit.html)
- [`CNormalizedImageElement`]({{ site.cpp_api }}normalized-image-element.html)
- [`CNormalizedImageUnit`]({{ site.cpp_api }}normalized-image-unit.html)

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

## Enumerations

- [`BufferOverflowProtectionMode`]({{ site.enumerations }}core/buffer-overflow-protection-mode.html?src=cpp)
- [`CapturedResultItemType`]({{ site.enumerations }}core/captured-result-item-type.html?src=cpp)
- [`CornerType`]({{ site.enumerations }}core/corner-type.html?src=cpp)
- [`ErrorCode`]({{ site.enumerations }}core/error-code.html?src=cpp)
- [`GrayscaleTransformationMode`]({{ site.enumerations }}core/grayscale-transformation-mode.html?src=cpp)
- [`ImageCaptureDistanceMode`]({{ site.enumerations }}core/image-capture-distance-mode.html?src=cpp)
- [`ImagePixelFormat`]({{ site.enumerations }}core/image-pixel-format.html?src=cpp)
- [`ImageSourceState`]({{ site.enumerations }}core/image-source-state.html?src=cpp)
- [`ImageTagType`]({{ site.enumerations }}core/image-tag-type.html?src=cpp)
- [`IntermediateResultUnitType`]({{ site.enumerations }}core/intermediate-result-unit-type.html?src=cpp)
- [`PDFReadingMode`]({{ site.enumerations }}core/pdf-reading-mode.html?src=cpp)
- [`RegionObjectElementType`]({{ site.enumerations }}core/region-object-element-type.html?src=cpp)
- [`SectionType`]({{ site.enumerations }}core/section-type.html?src=cpp)
- [`TargetType`]({{ site.enumerations }}core/target-type.html?src=cpp)
- [`VideoFrameQuality`]({{ site.enumerations }}core/video-frame-quality.html?src=cpp)
