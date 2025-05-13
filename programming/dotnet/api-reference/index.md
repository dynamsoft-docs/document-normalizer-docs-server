---
layout: default-layout
title: Dynamsoft Document Normalizer .NET API Reference - Main Page
description: This is the main page of Dynamsoft Document Normalizer SDK API Reference for .NET Language.
keywords: CDocumentNormalizer, api reference, .NET
---

# API Reference - .NET

## DynamsoftCaptureVisionRouter

### [CaptureVisionRouter]({{ site.dcvb_dotnet_api }}capture-vision-router/capture-vision-router.html)

- [`Constructor and Destructor`]({{ site.dcvb_dotnet_api }}capture-vision-router/instantiate.html)
- [`Single-File Processing`]({{ site.dcvb_dotnet_api }}capture-vision-router/single-file-processing.html)
- [`Multiple-File Processing`]({{ site.dcvb_dotnet_api }}capture-vision-router/multiple-file-processing.html)
- [`Settings`]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html)
- [`Auxiliary Methods`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-methods.html)

### Classes

- [`ICaptureStateListener`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CaptureVisionRouterModule`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CapturedResult`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result.html)
- [`CapturedResultFilter`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)
- [`CapturedResultReceiver`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)
- [`IImageSourceStateListener`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)
- [`PresetTemplate`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/preset-template.html)

### Structs

- [`SimplifiedCaptureVisionSettings`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

### Enums

- [`EnumCaptureState`]({{ site.dcvb_enumerations }}capture-vision-router/capture-state.html)
- [`EnumImageSourceState`]({{ site.dcvb_enumerations }}capture-vision-router/image-source-state.html)

## DynamsoftDocumentNormalizer

### Classes

- [`DetectedQuadResultItem`]({{ site.ddn_dotnet_api }}detected-quad-result-item.html)
- [`DetectedQuadsResult`]({{ site.ddn_dotnet_api }}detected-quads-result.html)
- [`DocumentNormalizerModule`]({{ site.ddn_dotnet_api }}document-normalizer-module.html)
- [`NormalizedImageResultItem`]({{ site.ddn_dotnet_api }}normalized-image-result-item.html)
- [`NormalizedImagesResult`]({{ site.ddn_dotnet_api }}normalized-images-result.html)

### Structs

- [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_dotnet_api }}simplified-document-normalizer-settings.html)

### Enums

- [`EnumImageColourMode`]({{ site.dcvb_enumerations }}document-normalizer/image-colour-mode.html)

## DynamsoftCore

### Classes

- [`CapturedResultItem`]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-item.html)
- [`CoreModule`]({{ site.dcvb_dotnet_api }}core/basic-classes/core-module.html)
- [`FileImageTag`]({{ site.dcvb_dotnet_api }}core/basic-classes/file-image-tag.html)
- [`ImageData`]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)
- [`ImageSourceAdapter`]({{ site.dcvb_dotnet_api }}core/basic-classes/image-source-adapter.html)
- [`IImageSourceErrorListener`]({{ site.dcvb_dotnet_api }}core/basic-classes/image-source-error-listener.html)
- [`ImageTag`]({{ site.dcvb_dotnet_api }}core/basic-classes/image-tag.html)
- [`LineSegment`]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)
- [`OriginalImageResultItem`]({{ site.dcvb_dotnet_api }}core/basic-classes/original-image-result-item.html)
- [`PDFReadingParameter`]({{ site.dcvb_dotnet_api }}core/basic-classes/pdf-reading-parameter.html)
- [`Point`]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)
- [`Quadrilateral`]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)
- [`Rect`]({{ site.dcvb_dotnet_api }}core/basic-classes/rect.html)
- [`VideoFrameTag`]({{ site.dcvb_dotnet_api }}core/basic-classes/video-frame-tag.html)

### Structs


### Enums

- [`EnumBufferOverflowProtectionMode`]({{ site.dcvb_enumerations }}core/buffer-overflow-protection-mode.html)
- [`EnumCapturedResultItemType`]({{ site.dcvb_enumerations }}core/captured-result-item-type.html)
- [`EnumColourChannelUsageType`]({{ site.dcvb_enumerations }}core/colour-channel-usage-type.html)
- [`EnumErrorCode`]({{ site.dcvb_enumerations }}core/error-code.html)
- [`EnumGrayscaleEnhancementMode`]({{ site.dcvb_enumerations }}core/grayscale-enhancement-mode.html)
- [`EnumGrayscaleTransformationMode`]({{ site.dcvb_enumerations }}core/grayscale-transformation-mode.html)
- [`EnumImageCaptureDistanceMode`]({{ site.dcvb_enumerations }}core/image-capture-distance-mode.html)
- [`EnumImagePixelFormat`]({{ site.dcvb_enumerations }}core/image-pixel-format.html)
- [`EnumImageTagType`]({{ site.dcvb_enumerations }}core/image-tag-type.html)
- [`EnumPDFReadingMode`]({{ site.dcvb_enumerations }}core/pdf-reading-mode.html)
- [`EnumRasterDataSource`]({{ site.dcvb_enumerations }}core/raster-data-source.html)
- [`EnumVideoFrameQuality`]({{ site.dcvb_enumerations }}core/video-frame-quality.html)

## DynamsoftUtility

- [`DirectoryFetcher`]({{ site.dcvb_dotnet_api }}utility/directory-fetcher.html)
- [`FileFetcher`]({{ site.dcvb_dotnet_api }}utility/file-fetcher.html)
- [`ImageManager`]({{ site.dcvb_dotnet_api }}utility/image-manager.html)
- [`MultiFrameResultCrossFilter`]({{ site.dcvb_dotnet_api }}utility/multi-frame-result-cross-filter.html)
- [`ProactiveImageSourceAdapter`]({{ site.dcvb_dotnet_api }}utility/proactive-image-source-adapter.html)
- [`UtilityModule`]({{ site.dcvb_dotnet_api }}utility/utility-module.html)

## DynamsoftLicense

- [`LicenseManager`]({{ site.dcvb_dotnet_api }}license/license-manager.html)
- [`LicenseModule`]({{ site.dcvb_dotnet_api }}license/license-module.html)


## DynamsoftImageProcessing

- [`ImageProcessingModule`]({{ site.dcvb_dotnet_api }}image-processing/image-processing-module.html)

