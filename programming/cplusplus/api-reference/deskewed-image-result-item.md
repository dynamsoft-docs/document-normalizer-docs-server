---
layout: default-layout
title: CDeskewedImageResultItem Class
description: This page shows CDeskewedImageResultItem class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetImageData, SaveToFile, CDeskewedImageResultItem, api reference
---

# CDeskewedImageResultItem Class

The `CDeskewedImageResultItem` class stores a captured result item whose type is Deskewed image.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDeskewedImageResultItem: CCapturedResultItem
```

*Inheritance:* [CCapturedResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html) -> CDeskewedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetImageData`](#getimagedata) | Gets the ImageData of current object. |
| [`GetSourceDeskewQuad`](#getsourcedeskewquad)| Gets the quadrilateral used for deskewing the image. |
| [`GetCrossVerificationStatus`](getcrossverificationstatus)| Gets the status of current object as a verified deskewed image. |
| [`SetCrossVerificationStatus`](setcrossverificationstatus)| Sets the status of current object. |
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

### GetSourceDeskewQuad

Gets the quadrilateral used for deskewing the image.

```cpp
virtual CQuadrilateral GetSourceDeskewQuad() const = 0;
```

**Return Value**

A `CQuadrilateral` object representing the four corners of the quadrilateral used to deskew the image.

**See Also**

* [CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

### GetCrossVerificationStatus

Gets the status of current object as a verified deskewed image.

```cpp
virtual CrossVerificationStatus GetCrossVerificationStatus() const = 0;
```

**Return Value**

Return the CrossVerificationStatus of the deskewed image result.

### SetCrossVerificationStatus

Sets the status of current object.

```cpp
virtual void SetCrossVerificationStatus(CrossVerificationStatus status) = 0;
```

**Parameters**

`[in] status` The CrossVerificationStatus to be set.

### GetOriginalToLocalMatrix

Gets the transformation matrix from the original image coordinate system to the local coordinate system.

```cpp
virtual void GetOriginalToLocalMatrix(double matrix[9]) const = 0;
```

**Parameters**

`[out] matrix` matrix A double array of size 9, representing the 3x3 transformation matrix that converts coordinates from the original image to the local image.