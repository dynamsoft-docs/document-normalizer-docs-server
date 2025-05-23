---
layout: default-layout
title: CDetectedQuadsResult Class
description: This page shows CDetectedQuadsResult class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetItemsCount, GetErrorCode, GetErrorString, GetItem, GetOriginalImageHashId, GetOriginalImageTag, CDetectedQuadsResult, api reference
permalink: /programming/cplusplus/api-reference/detected-quads-result.html
---

# CDetectedQuadsResult Class

The `CDetectedQuadsResult` class stores a captured result whose type is detected quads.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDetectedQuadsResult
```

## Methods

| Method | Description |
|--------|-------------|
| [`GetItemsCount`](#getitemscount) | Gets the number of detected quadrilaterals. |
| [`GetErrorCode`](#geterrorcode) | Gets the error code of the detection operation. |
| [`GetErrorString`](#geterrorstring) | Gets the error message of the detection operation. |
| [`GetItem`](#getitem) | Gets the detected quadrilateral item at a specified index. |
| [`HasItem`](#hasitem) | Check if the item is present in the array.|
| [`RemoveItem`](#removeitem) | Remove a specific item from the array in the detected quads.|
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Get the rotation transformation matrix of the original image relative to the rotated image.|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image. |
| [`operator[]`](#operator) | Gets the detected quadrilateral item at a specified index.|
| [`Retain`](#retain) | Increases the reference count of the CDetectedQuadsResult object. |
| [`Release`](#release) | Decreases the reference count of the CDetectedQuadsResult object. |

### GetItemsCount

Gets the number of detected quadrilaterals.

```cpp
int GetItemsCount()
```

**Return value**

Returns the number of detected quadrilaterals.

### GetErrorCode

Gets the error code of the detection operation.

```cpp
int GetErrorCode()
```

**Return value**

Returns the error code.

**See Also**

* [ErrorCode]({{ site.dcvb_enumerations }}core/error-code.html?src=cpp&&lang=cpp)

### GetErrorString

Gets the error message of the detection operation.

```cpp
const char* GetErrorString()
```

**Return value**

Returns a pointer to a null-terminated string that represents the error message.

### GetItem

Gets the detected quadrilateral item at a specified index.

```cpp
const CDetectedQuadResultItem* GetItem(int index) const
```

**Parameters**

`[in] index` The index of the detected quadrilateral to retrieve.

**Return value**

Returns a pointer to a CDetectedQuadResultItem object that represents the detected quadrilateral at the specified index.

**See Also**

* [CDetectedQuadResultItem](detected-quad-result-item.md)

### HasItem

Check if the item is present in the array.

```cpp
bool HasItem(const CDetectedQuadResultItem* item) const
```

**Parameters**

`[in] item` The specific item to check.

**Return value**

Returns a bool value indicating whether the item is present in the array or not.

### RemoveItem

Remove a specific item from the array in the detected quads.

```cpp
int RemoveItem(const CDetectedQuadResultItem* item)
```

**Parameters**

`[in] item` The specific item to remove.

**Return value**

Return value indicating whether the deletion was successful or not.

### GetRotationTransformMatrix

Get the rotation transformation matrix of the original image relative to the rotated image.

```cpp
void GetRotationTransformMatrix(double matrix[9]) const;
```

**Parameters**

`[out] matrix` A double array which represents the rotation transform matrix.

### GetOriginalImageHashId

Gets the hash ID of the original image.

```cpp
const char* GetOriginalImageHashId()
```

**Return value**

Returns a pointer to a null-terminated string that represents the hash ID of the original image.

### GetOriginalImageTag

Gets the tag of the original image.

```cpp
const CImageTag* GetOriginalImageTag()
```

**Return value**

Returns a pointer to a CImageTag object that represents the tag of the original image.

**See Also**

* [CImageTag]({{ site.dcvb_cpp_api }}core/basic-structures/image-tag.html)

### operator[]

Gets the detected quadrilateral item at a specified index.

```cpp
virtual const CDetectedQuadResultItem* operator[](int index) const = 0
```

**Parameters**

`[in] index` The zero-based index of the detected quadrilateral to retrieve.

**Return value**

Returns a pointer to a CDetectedQuadResultItem object that represents the detected quadrilateral at the specified index.

### Retain

Increases the reference count of the CDetectedQuadsResult object.

```cpp
virtual CDetectedQuadsResult* Retain() = 0;
```

**Return value**

An object of CDetectedQuadsResult.

### Release

Decreases the reference count of the CDetectedQuadsResult object.

```cpp
virtual void Release() = 0;
```
