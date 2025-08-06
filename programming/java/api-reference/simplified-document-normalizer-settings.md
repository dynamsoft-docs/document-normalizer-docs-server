---
layout: default-layout
title: SimplifiedDocumentNormalizerSettings Class - Dynamsoft Document Normalizer Module Java Edition API Reference
description: Definition of the SimplifiedDocumentNormalizerSettings class in Dynamsoft Document Normalizer Module Java Edition.
keywords: class, java, SimplifiedDocumentNormalizerSettings
---

# SimplifiedDocumentNormalizerSettings

The `SimplifiedDocumentNormalizerSettings` class contains settings for document normalization. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

```java
public class SimplifiedDocumentNormalizerSettings
```

## Attributes Summary

| Attribute  | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *int[]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *int[]* |
| [`colourMode`](#colourmode) | *int* |
| [`pageSize`](#pagesize) | *int[]* |
| [`brightness`](#brightness) | *int* |
| [`contrast`](#contrast) | *int* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* |
| [`minQuadrilateralAreaRatio`](#minquadrilateralarearatio) | *int* |
| [`expectedDocumentsCount`](#expecteddocumentscount) | *int* |

### grayscaleTransformationModes

Specifies how grayscale transformations should be applied, including whether to process inverted grayscale images and the specific transformation mode to use.

It is an array of 8 integers, where each integer represents a mode specified by the [`EnumGrayscaleTransformationMode`]({{ site.dcvb_java_api }}core/enum-grayscale-transformation-mode.html) enumeration.

View the parameter reference page of <a href="{{ site.dcvb_parameters_reference }}image-parameter/grayscale-transformation-modes.html?product=ddn&repoType=core" target="_blank">`GrayscaleTransformationModes`</a> for more detail about grayscale transformation modes.

### grayscaleEnhancementModes

Specifies how to enhance the quality of the grayscale image.

It is an array of 8 integers, where each integer represents a mode specified by the [`EnumGrayscaleEnhancementMode`]({{ site.dcvb_java_api }}core/enum-grayscale-enhancement-mode.html) enumeration.

View the parameter reference page of <a href="{{ site.dcvb_parameters_reference }}image-parameter/grayscale-enhancement-modes.html?product=ddn&repoType=core" target="_blank">`GrayscaleEnhancementModes`</a> for more detail about grayscale enhancement modes.

### colourMode

Specifies the colour mode of the output image.

It is a value of the [`EnumImageColourMode`]({{ site.ddn_java_api }}enum-image-colour-mode.html) enumeration.

View the parameter reference page of <a href="{{ site.dcvb_parameters_reference }}document-normalizer-task-settings/colour-mode.html?product=ddn&repoType=core" target="_blank">`ColourMode`</a> for more detail about colour mode.

**Default value**

0, which means output image in colour mode.

### pageSize

Specifies the page size (width by height in pixels) of the normalized image.

### brightness

Specifies the brightness of the normalized image.

**Value Range**

[-100,100]

**Default value**

0

### contrast

Specifies the contrast of the normalized image.

**Value Range**

[-100,100]

**Default value**

0

### maxThreadsInOneTask

Specifies the maximum available threads count in one document normalization task.

**Value Range**

[1, 256]

**Default value**

4

### scaleDownThreshold

Specifies the threshold for the image shrinking.

**Value Range**

[512, 0x7fffffff]

**Default Value**

2300

**Remarks**

If the shorter edge size is larger than the given threshold value, the library will calculate the required height and width of the barcode image and shrink the image to that size before detection. Otherwise, the library will perform document detection on the original image.

### minQuadrilateralAreaRatio

Specifies the minimum ratio between the target quadrilateral area and the total image area. Only those exceeding this value will be output (measured in percentages).

**Value Range**

[0, 100]

**Default Value**

0, which means no limitation.

### expectedDocumentsCount

Specifies the number of documents expected to be detected.

**Value Range**

[0, 0x7fffffff]

**Default Value**

1.

