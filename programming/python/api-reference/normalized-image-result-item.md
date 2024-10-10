---
layout: default-layout
title: NormalizedImageResultItem Class - Dynamsoft Document Normalizer Module Python Edition API Reference
description: Definition of NormalizedImageResultItem class in Dynamsoft Document Normalizer Module Python Edition.
keywords: get_image_data, get_location, NormalizedImageResultItem, api reference
---

# NormalizedImageResultItem Class

The `NormalizedImageResultItem` class stores a captured result item whose type is normalized image.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class NormalizedImageResultItem(dynamsoft_core.CapturedResultItem)
```

*Inheritance:* [CapturedResultItem]({{ site.dcv_python_api }}core/basic-classes/captured-result-item.html) -> NormalizedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`get_image_data`](#get_image_data) | Gets the ImageData of current object. |
| [`get_location`](#get_location) | Get the quadrilateral from which you get the normalized image result item. |

### get_image_data

Gets the image data of current object.

```python
def get_image_data(self) -> ImageData :
```

**Return Value**

The image data.

**See Also**

[ImageData]({{ site.dcv_python_api }}core/basic-classes/image-data.html)

### get_location

Gets the location of current object.

```python
def get_location(self) -> Quadrilateral:
```

**Return Value**

The location of current object.

**See Also**

[Quadrilateral]({{ site.dcv_python_api }}core/basic-classes/quadrilateral.html)
