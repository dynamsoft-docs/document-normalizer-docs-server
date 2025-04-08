---
layout: default-layout
title: SimplifiedDocumentNormalizerSettings Class - Dynamsoft Document Normalizer Module Python Edition API Reference
description: Definition of the SimplifiedDocumentNormalizerSettings class in Dynamsoft Document Normalizer Module Python Edition.
keywords: class, python, SimplifiedDocumentNormalizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# SimplifiedDocumentNormalizerSettings

The `SimplifiedDocumentNormalizerSettings` class contains settings for document normalization. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

```python
class SimplifiedDocumentNormalizerSettings
```

## Properties Summary

| Property  | Type |
| --------- | ---- |
| [`grayscale_transformation_modes`](#grayscale_transformation_modes) | *List[int]* |
| [`grayscale_enhancement_modes`](#grayscale_enhancement_modes) | *List[int]* |
| [`colour_mode`](#colour_mode) | *int* |
| [`page_size`](#page_size) | *List[int]* |
| [`brightness`](#brightness) | *int* |
| [`contrast`](#contrast) | *int* |
| [`max_threads_in_one_task`](#max_threads_in_one_task) | *int* |
| [`scale_down_threshold`](#scale_down_threshold) | *int* |
| [`min_quadrilateral_area_ratio`](#min_quadrilateral_area_ratio) | *int* |
| [`expected_documents_count`](#expected_documents_count) | *int* |

### grayscale_transformation_modes

Specifies how grayscale transformations should be applied, including whether to process inverted grayscale images and the specific transformation mode to use.

It is a list of 8 integers, where each integer represents a mode specified by the [`EnumGrayscaleTransformationMode`]({{ site.dcv_enumerations }}core/grayscale-transformation-mode.html?lang=python) enumeration.

View the parameter reference page of <a href="{{ site.dcv_parameters_reference }}image-parameter/grayscale-transformation-modes.html?product=ddn&repoType=core" target="_blank">`GrayscaleTransformationModes`</a> for more detail about grayscale transformation modes.

### grayscale_enhancement_modes

Specifies how to enhance the quality of the grayscale image.

It is a list of 8 integers, where each integer represents a mode specified by the [`EnumGrayscaleEnhancementMode`]({{ site.dcv_enumerations }}core/grayscale-enhancement-mode.html?lang=python) enumeration.

View the parameter reference page of <a href="{{ site.dcv_parameters_reference }}image-parameter/grayscale-enhancement-modes.html?product=ddn&repoType=core" target="_blank">`GrayscaleEnhancementModes`</a> for more detail about grayscale enhancement modes.

### colour_mode

Specifies the colour mode of the output image.

It is a value of the [`EnumImageColourMode`]({{ site.dcv_enumerations }}document-normalizer/image-colour-mode.html?lang=python) enumeration.

View the parameter reference page of <a href="{{ site.dcv_parameters_reference }}document-normalizer-task-settings/colour-mode.html?product=ddn&repoType=core" target="_blank">`ColourMode`</a> for more detail about colour mode.

**Default value**

0, which means output image in colour mode.

### page_size

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

### max_threads_in_one_task

Specifies the maximum available threads count in one document normalization task.

**Value Range**

[1, 256]

**Default value**

4

### scale_down_threshold

Specifies the threshold for the image shrinking.

**Value Range**

[512, 0x7fffffff]

**Default Value**

2300

**Remarks**

If the shorter edge size is larger than the given threshold value, the library will calculate the required height and width of the barcode image and shrink the image to that size before detection. Otherwise, the library will perform document detection on the original image.

### min_quadrilateral_area_ratio

Specifies the minimum ratio between the target quadrilateral area and the total image area. Only those exceeding this value will be output (measured in percentages).

**Value Range**

[0, 100]

**Default Value**

0, which means no limitation.

### expected_documents_count

Specifies the number of documents expected to be detected.

**Value Range**

[0, 0x7fffffff]

**Default Value**

0, which means the count is unknown. The library will try to find at least 1 document.

## Methods
  
| Method | Description |
|------- | ---- |
| [`__init__`](#__init__) | Initializes a new instance of the `SimplifiedDocumentNormalizerSettings` class. |

### \_\_init\_\_

Initializes a new instance of the `SimplifiedDocumentNormalizerSettings` class.

```python
def __init__(self):
```

