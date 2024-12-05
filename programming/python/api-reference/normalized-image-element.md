---
layout: default-layout
title: NormalizedImageElement Class
description: This page shows NormalizedImageElement class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_image_data, GetReferencedElement, NormalizedImageElement, api reference
---

# NormalizedImageElement Class

The `NormalizedImageElement` class stores an intermediate result whose type is normalized image.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class NormalizedImageElement(RegionObjectElement)
```

*Inheritance:* [RegionObjectElement]({{ site.dcv_python_api }}core/intermediate-results/region-object-element.html) -> NormalizedImageElement
## Methods

| Method | Description |
|--------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `NormalizedImageElement` class. |
| [`get_image_data`](#get_image_data) | Gets the ImageData of current object. |

### \_\_init\_\_

Initializes a new instance of the `NormalizedImageElement` class.

```python
def __init__(self, *args, **kwargs):
```

### get_image_data

Gets the image data of current object.

```python
def get_image_data(self) -> ImageData:
```

**Return Value**

The image data.

**See Also**

* [ImageData]({{ site.dcv_python_api }}core/basic-classes/image-data.html)
