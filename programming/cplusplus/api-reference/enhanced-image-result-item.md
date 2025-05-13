---
layout: default-layout
title: CEnhancedImageResultItem Class
description: This page shows CEnhancedImageResultItem class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetImageData, SaveToFile, CEnhancedImageResultItem, api reference
---

# CEnhancedImageResultItem Class

The `CEnhancedImageResultItem` class stores a captured result item whose type is Enhanced image.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CEnhancedImageResultItem: CCapturedResultItem
```

*Inheritance:* [CCapturedResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html) -> CEnhancedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetImageData`](#getimagedata) | Gets the ImageData of current object. |
| [`GetOriginalToLocalMatrix`](getoriginaltolocalmatrix) | Gets the transformation matrix from the original image coordinate system to the local coordinate system. |

### GetImageData

Gets the ImageData of current object.

```cpp
const CImageData* GetImageData() 
```

**Return Value**

The image data.

**See Also**

* [CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### GetOriginalToLocalMatrix

Gets the transformation matrix from the original image coordinate system to the local coordinate system.

```cpp
virtual void GetOriginalToLocalMatrix(double matrix[9]) const = 0;
```

**Parameters**

`[out] matrix` matrix A double array of size 9, representing the 3x3 transformation matrix that converts coordinates from the original image to the local image.