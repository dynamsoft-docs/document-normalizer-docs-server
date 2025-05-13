---
layout: default-layout
title: LogicLinesUnit Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows LogicLinesUnit class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetCount, GetLogicLine, LogicLinesUnit, api reference
---

# LogicLinesUnit Class

The `LogicLinesUnit` class represents an intermediate result unit whose type is logic lines. Logic lines are formed by combining long lines that meet certain conditions.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class LogicLinesUnit : IntermediateResultUnit, IEnumerable<LineSegment>
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> LogicLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of `LogicLine` objects in current object.|
| [`GetLogicLine`](#getlogicline) | Gets a `LogicLine` object from current object by specifying a index. |
| [`GetLogicLines`](#getlogiclines) | Gets all `LogicLine` objects from current object. |
| [`RemoveAllLogicLines`](#removealllogiclines) | Removes all the `LogicLine` objects in current object. |
| [`RemoveLogicLine`](#removelogicline) | Removes a `LogicLine` from current object by specifying an index. |
| [`AddLogicLine`](#addlogicline) | Adds a `LogicLine` to current object. |
| [`SetLogicLine`](#setlogicline) | Sets the `LogicLine` at the specified index. |

### GetCount

Gets the count of `LogicLine` objects in current object.

```csharp
int GetCount() 
```

**Return Value**

The count of `LogicLine` objects in current object.

### GetLogicLine

Gets a `LogicLine` object from current object by specifying a index.

```csharp
LineSegment GetLogicLine(int index)
```

**Parameters**

`[in] index` The index of the `LogicLine` object.

**Return Value**

Returns the `LogicLine` object.

**See Also**

* [LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### GetLogicLines

Gets all `LogicLine` objects from current object.

```csharp
LineSegment[] GetLogicLines()
```

**Return Value**

Returns all the `LogicLine` objects.

**See Also**

* [LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### RemoveAllLogicLines

Removes all the `LogicLine`s in current object.

```csharp
void RemoveAllLogicLines()
```

### RemoveLogicLine

Removes a `LogicLine` from current object by specifying an index.

```csharp
int RemoveLogicLine(int index)
```

**Parameters**

`[in] index` The index of the `LogicLine` to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddLogicLine

Adds a `LogicLine` to current object.

```csharp
int AddLogicLine(LineSegment logicline, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] line` the `LogicLine` to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### SetLogicLine

Sets the `LogicLine` at the specified index.

```csharp
int SetLogicLine(int index, LineSegment logicline, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] index` The index of the `LogicLine` to be set.

`[in] logicline` the `LogicLine` to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)
