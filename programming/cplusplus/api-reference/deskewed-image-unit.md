---
layout: default-layout
title: CDeskewedImagesUnit Class
description: This page shows CDeskewedImagesUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetDeskewedImage, CDeskewedImagesUnit, api reference
permalink: /programming/cplusplus/api-reference/Deskewed-image-unit.html
---

# CDeskewedImagesUnit Class

The `CDeskewedImagesUnit` class represents an intermediate result unit whose type is Deskewed images.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDeskewedImagesUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CDeskewedImagesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetDeskewedImage`](#getdeskewedimage) | Gets a DeskewedImage object from current object. |
| [`SetDeskewedImage`](#setdeskewedimage) | Sets the Deskewed image. |
| **Methods Inherited from [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html):** | |
| [`GetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit.|
| [`GetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the image tag of the original image. |
| [`GetType`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`SetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#sethashid) | Sets the hash ID of the unit. |
| [`SetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagehashid) | Sets the hash ID of the original image. |
| [`SetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagetag) | Sets the image tag of the original image. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#retain) | Increases the reference count of the unit. |
| [`Release`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#release) | Decreases the reference count of the unit. |
| [`GetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via TransformMatrixType. |
| [`SetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#settransformmatrix) | Sets the transformation matrix via TransformMatrixType. |

### GetDeskewedImage

Gets a DeskewedImage object from current unit.

```cpp
virtual const CDeskewedImageElement* GetDeskewedImage() const = 0;
```

**Return Value**

Returns the `CDeskewedImageElement` object.

**See Also**

* [CDeskewedImageElement]({{ site.ddn_cpp_api }}deskewed-image-element.html)

### SetDeskewedImage

Sets the Deskewed image.

```cpp
virtual int SetDeskewedImage(const CDeskewedImageElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] element` The Deskewed image to be set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.