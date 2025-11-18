---
layout: default-layout
title: CLogicLinesUnit Class
description: This page shows CLogicLinesUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetCount, GetLogicLine, CLogicLinesUnit, api reference
permalink: /programming/cplusplus/api-reference/logic-lines-unit.html
---

# CLogicLinesUnit Class

The `CLogicLinesUnit` class represents an intermediate result unit whose type is logic lines. Logic lines are formed by combining long lines that meet certain conditions.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CLogicLinesUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CLogicLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of LogicLine objects in current object.|
| [`GetLogicLine`](#getlogicline) | Gets a LogicLine object from current object by specifying a index. |
| [`RemoveAllLogicLines`](#removealllogiclines) | Removes all the LogicLines in current object. |
| [`RemoveLogicLine`](#removelogicline) | Removes a LogicLine from current object by specifying an index. |
| [`AddLogicLine`](#addlogicline) | Adds a LogicLine to current object. |
| [`SetLogicLine`](#setlogicline) | Sets the LogicLine at the specified index. |
| Methods Inherited from [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html): | |
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

Gets the count of LogicLine objects in current object.

```cpp
int GetCount() 
```

**Return Value**

The count of LogicLine objects in current object.

### GetLogicLine

Gets a LogicLine object from current object by specifying a index.

```cpp
const CLineSegment* GetLogicLine(int index) const = 0;
```

**Parameters**

`[in] index` The index of the LogicLine object.

**Return Value**

Returns the LogicLine object.

**See Also**

* [CLineSegment]({{ site.dcvb_cpp_api }}core/basic-structures/line-segment.html)
* [ErrorCode]({{ site.dcvb_cpp_api }}core/enum-error-code.html)

### RemoveAllLogicLines

Removes all the LogicLines in current object.

```cpp
virtual void RemoveAllLogicLines() = 0
```

### RemoveLogicLine

Removes a LogicLine from current object by specifying an index.

```cpp
virtual int RemoveLogicLine(int index) = 0
```

**Parameters**

`[in] index` The index of the LogicLine to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddLogicLine

Adds a LogicLine to current object.

```cpp
virtual int AddLogicLine(const CLineSegment& logicline, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0
```

**Parameters**

`[in] line` The LogicLine to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### SetLogicLine

Sets the LogicLine at the specified index.

```cpp
virtual int SetLogicLine(int index, const CLineSegment& logicline, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] index` The index of the LogicLine to be set.

`[in] line` The LogicLine to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.
