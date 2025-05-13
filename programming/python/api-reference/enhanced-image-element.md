---
layout: default-layout
title: EnhancedImageElement Class
description: This page shows EnhancedImageElement class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: set_image_data, EnhancedImageElement, api reference
---

# EnhancedImageElement Class

The `EnhancedImageElement` class stores an intermediate result whose type is Enhanced image.

## Definition

*Module:* dynamsoft_document_normalizer

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
