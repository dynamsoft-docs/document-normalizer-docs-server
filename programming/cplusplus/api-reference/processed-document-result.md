---
layout: default-layout
title: CProcessedDocumentResult Class
description: This page shows CProcessedDocumentResult class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: CProcessedDocumentResult, api reference
---

# CProcessedDocumentResult Class

The `CProcessedDocumentResult` class is a base class for storing processed document results, including detected quads, deskewed images, and enhanced images. It inherits from `CCapturedResultBase`.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CProcessedDocumentResult : CCapturedResultBase
```

*Inheritance:* [CCapturedResultBase]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html) -> CProcessedDocumentResult

## Methods

| Method | Description |
|--------|-------------|
| [`GetDetectedQuadResultItemsCount`](#getdetectedquadresultitemscount)   |	Gets the count of detected quad result items.                        |
| [`GetDeskewedImageResultItemsCount`](#getdeskewedimageresultitemscount) |	Gets the count of deskewed image result items.                       |
| [`GetEnhancedImageResultItemsCount`](#getenhancedimageresultitemscount) |	Gets the count of enhanced image result items.                       |
| [`GetDeskewedImageResultItem`](#getdeskewedimageresultitem)	          | Retrieves the deskewed image result item at the specified index.     |
| [`GetDetectedQuadResultItem`](#getdetectedquadresultitem)	              | Retrieves the detected quad result item at the specified index.      |
| [`GetEnhancedImageResultItem`](#getenhancedimageresultitem)	          | Retrieves the enhanced image result item at the specified index.     |
| [`Retain`](#retain)	                                                  | Increases the reference count of the CProcessedDocumentResult object.|
| [`Release`](#release)	                                                  | Decreases the reference count of the CProcessedDocumentResult object.|
| [`RemoveItem`](#removeitem)	                                          | Removes a specific item from the array in the recognition result.    |
| [`HasItem`](#hasitem)	                                                  | Checks if a specific item is present in the array.                   |
| **Methods Inherited from [CCapturedResultBase]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html):** | |
| [`GetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#getoriginalimagetag) | Gets the tag of the original image. |
| [`GetRotationTransformMatrix`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#getrotationtransformmatrix) | Gets the rotation transformation matrix of the original image relative to the rotated image. |
| [`GetErrorCode`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#geterrorcode) | Gets the error code of the recognition result, if an error occurred. |
| [`GetErrorString`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#geterrorstring) | Gets the error message of the recognition result, if an error occurred. |

### GetDetectedQuadResultItemsCount

Gets the count of detected quad result items.

```cpp
virtual int GetDetectedQuadResultItemsCount() const = 0;
```

**Return Value**

Returns the number of detected quad result items.

### GetDeskewedImageResultItemsCount

Gets the count of deskewed image result items.

```cpp
virtual int GetDeskewedImageResultItemsCount() const = 0;
```

**Return Value**

Returns the number of deskewed image result items.

### GetEnhancedImageResultItemsCount

Gets the count of enhanced image result items.

```cpp
virtual int GetEnhancedImageResultItemsCount() const = 0;
```

**Return Value**

Returns the number of enhanced image result items.

### GetDeskewedImageResultItem

Retrieves the deskewed image result item at the specified index.

```cpp
virtual const CDeskewedImageResultItem* GetDeskewedImageResultItem(int index) const = 0;
```

**Parameters**

`[in] index` The index of the deskewed image result item to retrieve.

**Return Value**

Returns a pointer to a CDeskewedImageResultItem object representing the deskewed image result at the specified index.

### GetDetectedQuadResultItem

Retrieves the detected quad result item at the specified index.

```cpp
virtual const CDetectedQuadResultItem* GetDetectedQuadResultItem(int index) const = 0;
```

**Parameters**

`[in] index` The index of the detected quad result item to retrieve.

**Return Value**

Returns a pointer to a CDetectedQuadResultItem object representing the detected quad result at the specified index.

### GetEnhancedImageResultItem

Retrieves the enhanced image result item at the specified index.

```cpp
virtual const CEnhancedImageResultItem* GetEnhancedImageResultItem(int index) const = 0;
```

**Parameters**

`[in] index` The index of the enhanced image result item to retrieve.

**Return Value**

Returns a pointer to a CEnhancedImageResultItem object representing the enhanced image result at the specified index.

### Retain

Increases the reference count of the CProcessedDocumentResult object.

```cpp
virtual CProcessedDocumentResult* Retain() = 0;
```

**Return Value**

Returns an object of CProcessedDocumentResult.

### Release

Decreases the reference count of the CProcessedDocumentResult object.

```cpp
virtual void Release() = 0;
```

### RemoveItem

Removes a specific item from the array in the recognition result.

```cpp
virtual int RemoveItem(const CDetectedQuadResultItem* item) = 0;
virtual int RemoveItem(const CDeskewedImageResultItem* item) = 0;
virtual int RemoveItem(const CEnhancedImageResultItem* item) = 0;
```

`Parameters`

`[in] item` The specific item to remove.

**Return Value**

Returns a value indicating whether the deletion was successful or not.

### HasItem

Checks if a specific item is present in the array.

```cpp
virtual bool HasItem(const CDetectedQuadResultItem* item) const = 0;
virtual bool HasItem(const CDeskewedImageResultItem* item) const = 0;
virtual bool HasItem(const CEnhancedImageResultItem* item) const = 0;
```

**Parameters**

`[in] item` The specific item to check.

**Return Value**

Returns a bool value indicating whether the item is present in the array or not.