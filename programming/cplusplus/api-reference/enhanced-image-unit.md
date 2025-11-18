---
layout: default-layout
title: CEnhancedImagesUnit Class
description: This page shows CEnhancedImagesUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetEnhancedImage, CEnhancedImagesUnit, api reference
---

# CEnhancedImagesUnit Class

The `CEnhancedImagesUnit` class represents an intermediate result unit whose type is enhanced images.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CEnhancedImagesUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CEnhancedImagesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetEnhancedImage`](#getenhancedimage) | Gets a enhancedImage object from current object. |
| [`SetEnhancedImage`](#setenhancedimage) | Sets the enhanced image. |
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

### GetEnhancedImage

Gets a enhancedImage object from current unit.

```cpp
virtual const CEnhancedImageElement* GetEnhancedImage() const = 0;
```

**Return Value**

Returns the `CEnhancedImageElement` object.

**See Also**

* [CEnhancedImageElement]({{ site.ddn_cpp_api }}enhanced-image-element.html)

### SetEnhancedImage

Sets the enhanced image.

```cpp
virtual int SetEnhancedImage(const CEnhancedImageElement* element) = 0;  
```

**Parameters**

`[in] element` The enhanced image to be set.

**Return value**

Returns 0 if successful, otherwise returns a negative value.