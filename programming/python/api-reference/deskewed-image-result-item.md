---
layout: default-layout
title: DeskewedImageResultItem Class
description: This page shows DeskewedImageResultItem class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_image_data, get_source_deskew_quad, get_cross_verification_status, get_original_to_local_matrix, DeskewedImageResultItem, api reference
---

# DeskewedImageResultItem Class

The `DeskewedImageResultItem` class stores a captured result item whose type is Deskewed image.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class DeskewedImageResultItem(CapturedResultItem):
```

*Inheritance:* [CapturedResultItem]({{ site.dcv_python_api }}core/basic-classes/captured-result-item.html) -> DeskewedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`get_image_data`](#get_image_data) | Gets the ImageData of current object. |
| [`get_source_deskew_quad`](#get_source_deskew_quad)| Gets the quadrilateral used for deskewing the image. |
| [`get_cross_verification_status`](get_cross_verification_status)| Gets the status of current object as a verified deskewed image. |
| [`get_original_to_local_matrix`](get_original_to_local_matrix) | Gets the transformation matrix from the original image coordinate system to the local coordinate system. |

### get_image_data

Gets the ImageData of current object.

```python
def get_image_data(self) -> ImageData: 
```

**Return Value**

The image data.

**See Also**

* [ImageData]({{ site.dcv_python_api }}core/basic-classes/image-data.html)

### get_source_deskew_quad

Gets the quadrilateral used for deskewing the image.

```python
def get_source_deskew_quad(self) -> Quadrilateral:
```

**Return Value**

A `Quadrilateral` object representing the four corners of the quadrilateral used to deskew the image.

**See Also**

* [Quadrilateral]({{ site.dcv_python_api }}core/basic-classes/quadrilateral.html)

### get_cross_verification_status

Gets the status of current object as a verified deskewed image.

```python
def get_cross_verification_status(self) -> EnumCrossVerificationStatus:
```

**Return Value**

Return the status of current object as a verified deskewed image.

**See Also**

[EnumCrossVerificationStatus]({{ site.dcv_python_api }}core/enum-cross-verification-status.html)

### get_original_to_local_matrix

Gets the transformation matrix from the original image coordinate system to the local coordinate system.

```python
def get_original_to_local_matrix(self) -> List[float]:
```

**Parameters**

A double array of size 9, representing the 3x3 transformation matrix that converts coordinates from the original image to the local image.