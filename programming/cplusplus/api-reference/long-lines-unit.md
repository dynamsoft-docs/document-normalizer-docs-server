---
layout: default-layout
title: CLongLinesUnit Class
description: This page shows CLongLinesUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetCount, GetLongLine, CLongLinesUnit, api reference
permalink: /programming/cplusplus/api-reference/long-lines-unit.html
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
| [`RemoveAllLongLines`](#removealllonglines) | Removes all the LongLines in current object. |
| [`RemoveLongLine`](#removelongline) | Removes a LongLine from current object by specifying an index. |
| [`AddLongLine`](#addlongline) | Adds a LongLine to current object. |
| [`SetLongLine`](#setlongline) | Sets the LongLine at the specified index. |

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

### RemoveAllLongLines

Removes all the LongLines in current object.

```cpp
virtual void RemoveAllLongLines() = 0
```

### RemoveLongLine

Removes a LongLine from current object by specifying an index.

```cpp
virtual int RemoveLongLine(int index) = 0
```

**Parameters**

`[in] index` The index of the LongLine to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddLongLine

Adds a LongLine to current object.

```cpp
virtual int AddLongLine(const CLineSegment& line, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0
```

**Parameters**

`[in] line` The LongLine to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### SetLongLine

Sets the LongLine at the specified index.

```cpp
virtual int SetLongLine(int index, const CLineSegment& line, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] index` The index of the LongLine to be set.

`[in] line` The LongLine to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.
