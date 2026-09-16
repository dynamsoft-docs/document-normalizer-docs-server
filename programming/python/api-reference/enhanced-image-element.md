---
layout: default-layout
title: EnhancedImageElement Class
description: API reference for the EnhancedImageElement class in Dynamsoft Document Normalizer Python Edition, which represents an intermediate result element containing an enhanced (color-corrected) document image.
keywords: set_image_data, EnhancedImageElement, api reference
---

# EnhancedImageElement Class

The `EnhancedImageElement` class stores an intermediate result whose type is Enhanced image.

## Definition

*Module:* ddn

```python
class EnhancedImageElement(RegionObjectElement):
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html) -> EnhancedImageElement

## Methods

| Method | Description |
|--------|-------------|
| [`set_image_data`](#set_image_data) | Sets the image data of the Enhanced image element. |

### set_image_data

Sets the image data of the Enhanced image element.

```python
def set_image_data(self, image_data: ImageData) -> int:
```

**Parameters**

`image_data`  The image data to set.

**Return Value**

Returns 0 if succeeds, nonzero otherwise. 

**See Also**

* [ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)
