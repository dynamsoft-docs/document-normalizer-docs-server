---
layout: default-layout
title: CCornersUnit Class
description: This page shows CCornersUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetCount, GetCorner, CCornersUnit, api reference
permalink: /programming/cplusplus/api-reference/corners-unit.html
---

# CCornersUnit Class

The CCornersUnit class represents an intermediate result unit whose type is corners.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CCornersUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CCornersUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of Corner objects in current object.|
| [`GetCorner`](#getcorner) | Gets a Corner object from current object by specifying a index. |
| [`RemoveAllCorners`](#removeallcorners) | Removes all the corners in current object. |
| [`RemoveCorner`](#removecorner) | Removes a corner from current object by specifying an index. |
| [`AddCorner`](#addcorner) | Adds a corner to current object. |
| [`SetCorner`](#setcorner) | Sets the corner at the specified index. |
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

### GetCount

Gets the count of Corner objects in current object.

```cpp
int GetCount() 
```

**Return Value**

The count of Corner objects in current object.

### GetCorner

Gets a Corner object from current object by specifying a index.

```cpp
int GetCorner(int index, CCorner* corner)
```

**Parameters**

`[in] index` The index of the Corner object.

`[in, out] corner` The Corner object got by the specific index.

**Return Value**

Returns the error code.

**See Also**

* [CCorner]({{ site.dcvb_cpp_api }}core/basic-structures/corner.html)
* [ErrorCode]({{ site.dcvb_cpp_api }}core/enum-error-code.html)

### RemoveAllCorners

Removes all the corners in current object.

```cpp
virtual void RemoveAllCorners() = 0
```

### RemoveCorner

Removes a corner from current object by specifying an index.

```cpp
virtual int RemoveCorner(int index) = 0
```

**Parameters**

`[in] index` The index of the corner to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddCorner

Adds a corner to current object.

```cpp
virtual int AddCorner(const CCorner& corner, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0
```

**Parameters**

`[in] corner` The corner to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### SetCorner

Sets the corner at the specified index.

```cpp
virtual int SetCorner(int index, const CCorner& corner, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] index` The index of the corner to be set.

`[in] corner` The corner to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.
