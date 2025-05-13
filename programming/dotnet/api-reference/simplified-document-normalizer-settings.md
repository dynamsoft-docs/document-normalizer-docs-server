---
layout: default-layout
title: SimplifiedDocumentNormalizerSettings Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: Definition of the SimplifiedDocumentNormalizerSettings class in Dynamsoft Document Normalizer Module .NET Edition.
keywords: class, .NET, SimplifiedDocumentNormalizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# SimplifiedDocumentNormalizerSettings

The `SimplifiedDocumentNormalizerSettings` class contains settings for document normalization. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

```csharp
public class SimplifiedDocumentNormalizerSettings
```

## Attributes Summary

| Attribute | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *EnumGrayscaleTransformationMode[]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *EnumGrayscaleEnhancementMode[]* |
| [`colourMode`](#colourmode) | *EnumImageColourMode* |
| [`pageSize`](#pagesize) | *int[]* |
| [`brightness`](#brightness) | *int* |
| [`contrast`](#contrast) | *int* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* |
| [`minQuadrilateralAreaRatio`](#minquadrilateralarearatio) | *int* |
| [`expectedDocumentsCount`](#expecteddocumentscount) | *int* |

### grayscaleTransformationModes

Sets the grayscale transformation modes using an [`EnumGrayscaleTransformationMode`]({{ site.dcvb_dotnet_api }}core/enum-grayscale-transformation-mode.html) array with 8 elements. View the reference page of <a href="{{ site.dcvb_parameters_reference }}image-parameter/grayscale-transformation-modes.html">`GrayscaleTransformationModes`</a> for more detail about grayscale transformation modes.

```csharp
EnumGrayscaleTransformationMode[] grayscaleTransformationModes;
```

### grayscaleEnhancementModes

Sets the grayscale enhancement modes using an [`EnumGrayscaleEnhancementMode`]({{ site.dcvb_dotnet_api }}core/enum-grayscale-enhancement-mode.html) array with 8 elements. View the reference page of <a href="{{ site.dcvb_parameters_reference }}image-parameter/grayscale-enhancement-modes.html">`GrayscaleEnhancementModes`</a> for more detail about grayscale enhancement modes.

```csharp
EnumGrayscaleEnhancementMode[] grayscaleEnhancementModes;
```

### colourMode

Sets the output image colour mode using an enumeration value from [`EnumImageColourMode`]({{ site.ddn_dotnet_api }}core/enum-image-colour-mode.html).

```csharp
EnumImageColourMode colourMode;
```

**Default value**

"ICM_COLOUR"

### pageSize

Sets the page size (width by height in pixels) of the normalized image.

```csharp
int[] pageSize;
```

### brightness

Sets the brightness of the normalized image.

```csharp
int brightness;
```

**Value Range**

[-100,100]

**Default value**

0

### contrast

Sets the contrast of the normalized image.

```csharp
int contrastl
```

**Value Range**

[-100,100]

**Default value**

0

### maxThreadsInOneTask

Sets the maximum available threads count in one document normalization task.

```csharp
int maxThreadsInOneTask;
```

**Value Range**

[1, 256]

**Default value**

4

### scaleDownThreshold

Sets the threshold for the image shrinking.

```csharp
int scaleDownThreshold;
```

**Value Range**

[512, 0x7fffffff]

**Default Value**

2300

**Remarks**

If the shorter edge size is larger than the given threshold value, the library will calculate the required height and width of the barcode image and shrink the image to that size before detection. Otherwise, the library will perform document detection on the original image.

### minQuadrilateralAreaRatio

Sets the minimum ratio between the target document area and the total image area. Only those exceeding this value will be output (measured in percentages).

```csharp
int minQuadrilateralAreaRatio;
```

**Value Range**

[0, 100]

**Default value**

0

### expectedDocumentsCount

Sets the number of documents expected to be detected.

```csharp
int expectedDocumentsCount;
```

**Value Range**

[0, 0x7fffffff]

**Default value**

1
