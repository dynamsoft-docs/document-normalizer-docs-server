---
layout: default-layout
title: CDetectedQuadsUnit Class
description: This page shows CDetectedQuadsUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetCount, GetDetectedQuad, CDetectedQuadsUnit, api reference
permalink: /programming/cplusplus/api-reference/detected-quads-unit.html
---

# CDetectedQuadsUnit Class

The CDetectedQuadsUnit class represents an intermediate result unit whose type is detected quads.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDetectedQuadsUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CDetectedQuadsUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of DetectedQuad objects in current object.|
| [`GetDetectedQuad`](#getdetectedquad) | Gets a DetectedQuad object from current object by specifying a index. |
| [`operator[]`](#operator) | Gets a DetectedQuad object from current object by specifying a index.|
| [`RemoveAllDetectedQuads`](#removealldetectedquads) | Removes all the detected quads in current object. |
| [`RemoveDetectedQuad`](removedetectedquad) | Removes a detected quad from current object by specifying an index. |
| [`AddDetectedQuad`](adddetectedquad) | Adds a detected quad to current object. |
| [`SetDetectedQuad`](setdetectedquad) | Sets the detected quad at the specified index. |

### GetCount

Gets the count of DetectedQuad objects in current object.

```cpp
int GetCount() 
```

**Return Value**

The count of DetectedQuad objects in current object.

### GetDetectedQuad

Gets a DetectedQuad object from current object by specifying a index.

```cpp
const CDetectedQuadElement* GetDetectedQuad(int index)
```

**Parameters**

`[in] index` The index of the DetectedQuad object.

**Return Value**

Returns the DetectedQuad object got by the specific index.

**See Also**

* [CDetectedQuadElement]({{cpp_api}}detected-quad-element.html)

### operator[]

Gets a DetectedQuad object from current object by specifying a index.

```cpp
virtual const CDetectedQuadElement* operator[](int index) const = 0
```

**Parameters**

`[in] index` The index of the DetectedQuad object.

**Return value**

Returns the DetectedQuad object got by the specific index.

### RemoveAllDetectedQuads

Removes all the DetectedQuads in current object.

```cpp
virtual void RemoveAllDetectedQuads() = 0
```

### RemoveDetectedQuad

Removes a detected quad from current object by specifying an index.

```cpp
virtual int RemoveDetectedQuad(int index) = 0
```

**Parameters**

`[in] index` The index of the detected quad to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddDetectedQuad

Adds a DetectedQuad to current object.

```cpp
virtual int AddDetectedQuad(const CDetectedQuadElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0
```

**Parameters**

`[in] element` The detected quad to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### SetDetectedQuad

Sets the DetectedQuad at the specified index.

```cpp
virtual int SetDetectedQuad(int index, const CDetectedQuadElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0
```

**Parameters**

`[in] index` The index of the detected quad to be set.

`[in] element` The detected quad to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.
