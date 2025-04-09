---
layout: default-layout
title: DeskewedImageElement Class
description: This page shows DeskewedImageElement class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: set_image_data, get_source_deskew_quad, DeskewedImageElement, api reference
---

# DeskewedImageElement Class

The `DeskewedImageElement` class stores an intermediate result whose type is Deskewed image.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class DeskewedImageElement(RegionObjectElement):
```

*Inheritance:* [RegionObjectElement]({{ site.dcv_python_api }}core/intermediate-results/region-object-element.html) -> DeskewedImageElement

## Methods

| Method | Description |
|--------|-------------|
| [`set_image_data`](#set_image_data) | Sets the image data of the deskewed image element. |
| [`get_source_deskew_quad`](#get_source_deskew_quad) | Gets the quadrilateral used for deskewing the image. |

### set_image_data

Sets the image data of the deskewed image element.

```python
def set_image_data(self, image_data: ImageData) -> int:
```

**Parameters**

`image_data`  The image data to set.

**Return Value**

Returns 0 if succeeds, nonzero otherwise. 

**See Also**

* [ImageData]({{ site.dcv_python_api }}core/basic-classes/image-data.html)

### get_source_deskew_quad

Gets the quadrilateral used for deskewing the image.

```python
def get_source_deskew_quad(self) -> Quadrilateral:
```

**Return Value**

Returns A `Quadrilateral` object representing the four corners of the quadrilateral used to deskew the image.

**See Also**

* [Quadrilateral]({{ site.dcv_python_api }}core/basic-classes/quadrilateral.html)
