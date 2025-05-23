---
layout: default-layout
title: CNormalizedImagesResult Class
description: This page shows CNormalizedImagesResult class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetItemsCount, GetErrorCode, GetErrorString, GetItem, GetOriginalImageHashId, GetOriginalImageTag, CNormalizedImagesResult, api reference
permalink: /programming/cplusplus/api-reference/normalized-images-result.html
---

# CNormalizedImagesResult

The `CNormalizedImagesResult` class stores a collection of captured result items whose type are normalized images.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CNormalizedImagesResult
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetItemsCount`](#getitemscount) | Gets the number of normalized images in the result. |
| [`GetErrorCode`](#geterrorcode) | Gets the error code of the operation. |
| [`GetErrorString`](#geterrorstring) | Gets the error message of the operation. |
| [`GetItem`](#getitem) | Gets a specific normalized image from the result. |
| [`HasItem`](#hasitem) | Check if the item is present in the array.|
| [`RemoveItem`](#removeitem) | Remove a specific item from the array in the normalized images.|
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Get the rotation transformation matrix of the original image relative to the rotated image.|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image, from which you get the normalized image. |
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image, from which you get the normalized image. |
| [`operator[]`](#operator) | Gets the normalized images result at a specified index.|
| [`Retain`](#retain) | Increases the reference count of the CDetectedQuadsResult object. |
| [`Release`](#release) | Decreases the reference count of the CDetectedQuadsResult object. |

### GetItemsCount

Gets the number of normalized images in the result.

```cpp
int GetItemsCount()
```

**Return value**

Returns the number of normalized images in the result.

### GetErrorCode

Gets the error code of the operation.

```cpp
int GetErrorCode()
```

**Return value**

Returns the error code of the operation. A non-zero value indicates an error occurred.

**See Also**

* [ErrorCode]({{ site.dcvb_enumerations }}core/error-code.html?src=cpp&&lang=cpp)

### GetErrorString

Gets the error message of the operation.

```cpp
const char* GetErrorString()
```

**Return value**

Returns the error message of the operation.

### GetItem

Gets a specific normalized image from the result.

```cpp
const CNormalizedImageResultItem* GetItem(int index)
```

**Parameters**

`[in] index` The index of the normalized image to get.

**Return value**

Returns a pointer to the normalized image at the specified index. If the index is out of range, returns nullptr.

**See Also**

* [CNormalizedImageResultItem](normalized-image-result-item.md)

### HasItem

Check if the item is present in the array.

```cpp
bool HasItem(const CNormalizedImageResultItem* item) const
```

**Parameters**

`[in] item` The specific item to check.

**Return value**

Returns a bool value indicating whether the item is present in the array or not.

### RemoveItem

Remove a specific item from the array in the normalized images.

```cpp
int RemoveItem(const CNormalizedImageResultItem* item)
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

Gets the hash ID of the original image that was normalized.

```cpp
const char* GetOriginalImageHashId()
```

**Return value**

Returns the hash ID of the original image that was normalized.

### GetOriginalImageTag

Gets the tag of the original image that was normalized.

```cpp
const CImageTag* GetOriginalImageTag()
```

**Return value**

Returns a pointer to the tag of the original image that was normalized.

**See Also**

* [CImageTag]({{ site.dcvb_cpp_api }}core/basic-structures/image-tag.html)

### operator[]

Gets a specific normalized image from the result.

```cpp
virtual const CNormalizedImageResultItem* operator[](int index) const= 0
```

**Parameters**

`[in] index` The index of the normalized image to get.

**Return value**

Returns a pointer to the normalized image at the specified index. If the index is out of range, returns nullptr.

### Retain

Increases the reference count of the CNormalizedImagesResult object.

```cpp
virtual CNormalizedImagesResult* Retain() = 0;
```

**Return value**

An object of CNormalizedImagesResult.

### Release

Decreases the reference count of the CNormalizedImagesResult object.

```cpp
virtual void Release() = 0;
```
