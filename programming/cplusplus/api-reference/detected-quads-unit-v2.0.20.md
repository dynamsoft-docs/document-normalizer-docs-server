---
layout: default-layout
title: CDetectedQuadsUnit Class
description: This page shows CDetectedQuadsUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetCount, GetDetectedQuad, CDetectedQuadsUnit, api reference
permalink: /programming/cplusplus/api-reference/detected-quads-unit-v2.0.20.html
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
