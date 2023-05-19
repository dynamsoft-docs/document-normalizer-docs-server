---
layout: default-layout
title: CNormalizedImagesResultArray Class
description: This page shows CNormalizedImagesResultArray class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetCount, GetResult, CNormalizedImagesResultArray, api reference
permalink: /programming/cplusplus/api-reference/normalized-images-result-array.html
---

# CNormalizedImagesResultArray Class

An array storing `CNormalizedImagesResult` objects.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CNormalizedImagesResultArray
```

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of normalized images results in the array.|
| [`GetResult`](#getresult) | Gets a normalized images result at a specified index.|

## GetCount

Gets the count of normalized images results in the array.

```cpp
int GetCount() 
```

**Return Value**

The count of normalized images results in the array.

## GetResult

Gets a normalized images result at a specified index.

```cpp
const CNormalizedImagesResult* GetResult(int index) 
```

**Parameters**

`[in] index` The index of the normalized images result to retrieve.

**Return Value**

Returns a pointer to a CNormalizedImagesResult object that represents the result at the specified index.

**See Also**

* [CNormalizedImagesResult](normalized-images-result.md)
