---
layout: default-layout
title: CDetectedQuadsResultArray Class
description: API reference for the CDetectedQuadsResultArray class in Dynamsoft Document Normalizer C++ Edition, which provides an array of detected quadrilateral results.
keywords: GetCount, GetResult, CDetectedQuadsResultArray, api reference
permalink: /programming/cplusplus/api-reference/detected-quads-result-array.html
---

# CDetectedQuadsResultArray Class

An array storing `CDetectedQuadsResult` objects.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDetectedQuadsResultArray
```

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of detected quads results in the array.|
| [`GetResult`](#getresult) | Gets a detected quads result at a specified index.|

### GetCount

Gets the count of detected quads results in the array.

```cpp
int GetCount() 
```

**Return Value**

The count of detected quads results in the array.

### GetResult

Gets a detected quads result at a specified index.

```cpp
const CDetectedQuadsResult* GetResult(int index) 
```

**Parameters**

`[in] index` The index of the detected quads result to retrieve.

**Return Value**

Returns a pointer to a CDetectedQuadsResult object that represents the result at the specified index.

**See Also**

* [CDetectedQuadsResult](detected-quads-result.md)
