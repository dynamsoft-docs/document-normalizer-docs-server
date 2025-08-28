---
layout: default-layout
title: EnhancedImageResultItem Class
description: This page shows EnhancedImageResultItem class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_image_data, get_original_to_local_matrix, EnhancedImageResultItem, api reference
---

# EnhancedImageResultItem Class

The `EnhancedImageResultItem` class stores a captured result item whose type is Enhanced image.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class EnhancedImageResultItem(CapturedResultItem):
```

*Inheritance:* [CapturedResultItem]({{ site.dcvb_python_api }}core/basic-classes/captured-result-item.html) -> EnhancedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`get_image_data`](#get_image_data) | Gets the ImageData of current object. |
| [`get_original_to_local_matrix`](#get_original_to_local_matrix) | Gets the transformation matrix from the original image coordinate system to the local coordinate system. |

### get_image_data

Gets the ImageData of current object.

```python
def get_image_data(self) -> ImageData: 
```

**Return Value**

The image data.

**See Also**

* [ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### get_original_to_local_matrix

Gets the transformation matrix from the original image coordinate system to the local coordinate system.

```python
def get_original_to_local_matrix(self) -> List[float]:
```

**Parameters**

A double array of size 9, representing the 3x3 transformation matrix that converts coordinates from the original image to the local image.