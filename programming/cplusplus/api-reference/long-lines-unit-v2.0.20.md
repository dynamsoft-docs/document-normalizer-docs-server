---
layout: default-layout
title: CLongLinesUnit Class
description: This page shows CLongLinesUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetCount, GetLongLine, CLongLinesUnit, api reference
permalink: /programming/cplusplus/api-reference/long-lines-unit-v2.0.20.html
---

# CLongLinesUnit Class

The CLongLinesUnit class represents an intermediate result unit whose type is long lines. Short line segments that are located in the same line are extended and merged to form a long line segment.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CLongLinesUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CLongLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of LongLine objects in current object.|
| [`GetLongLine`](#getlongline) | Gets a LongLine object from current object by specifying a index. |

### GetCount

Gets the count of LongLine objects in current object.

```cpp
int GetCount() 
```

**Return Value**

The count of LongLine objects in current object.

### GetLongLine

Gets a LongLine object from current object by specifying a index.

```cpp
const CLineSegment* GetLongLine(int index) const = 0;
```

**Parameters**

`[in] index` The index of the LongLine object.

**Return Value**

Returns the LongLine object.

**See Also**

* [CLineSegment]({{ site.dcv_cpp_api }}core/basic-structures/line-segment.html)
* [ErrorCode]({{ site.enumerations }}core/error-code.html?src=cpp&&lang=cpp)
