---
layout: default-layout
title: LongLinesUnit Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows LongLinesUnit class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetCount, GetLongLine, LongLinesUnit, api reference
---

# LongLinesUnit Class

The `LongLinesUnit` class represents an intermediate result unit whose type is long lines. Short line segments that are located in the same line are extended and merged to form a long line segment.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class LongLinesUnit : IntermediateResultUnit, IEnumerable<LineSegment>
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> LongLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of `LongLine` objects in current object.|
| [`GetLongLine`](#getlongline) | Gets a `LongLine` object from current object by specifying a index. |
| [`GetLongLines`](#getlonglines) | Gets all `LongLine` objects from current object. |
| [`RemoveAllLongLines`](#removealllonglines) | Removes all the `LongLine` objects in current object. |
| [`RemoveLongLine`](#removelongline) | Removes a `LongLine` from current object by specifying an index. |
| [`AddLongLine`](#addlongline) | Adds a `LongLine` to current object. |
| [`SetLongLine`](#setlongline) | Sets the `LongLine` at the specified index. |

### GetCount

Gets the count of `LongLine` objects in current object.

```csharp
int GetCount() 
```

**Return Value**

The count of `LongLine` objects in current object.

### GetLongLine

Gets a `LongLine` object from current object by specifying a index.

```csharp
LineSegment GetLongLine(int index)
```

**Parameters**

`[in] index` The index of the `LongLine` object.

**Return Value**

Returns the `LongLine` object.

**See Also**

* [LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### GetLongLines

Gets all `LongLine` objects from current object.

```csharp
LineSegment[] GetLongLines()
```

**Return Value**

Returns all the `LongLine` objects.

**See Also**

* [LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### RemoveAllLongLines

Removes all the `LongLine` objects in current object.

```csharp
void RemoveAllLongLines()
```

### RemoveLongLine

Removes a `LongLine` from current object by specifying an index.

```csharp
int RemoveLongLine(int index)
```

**Parameters**

`[in] index` The index of the `LongLine` to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddLongLine

Adds a `LongLine` to current object.

```csharp
int AddLongLine(LineSegment line, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] line` The `LongLine` to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### SetLongLine

Sets the `LongLine` at the specified index.

```csharp
int SetLongLine(int index, LineSegment line, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] index` The index of the `LongLine` to be set.

`[in] line` The `LongLine` to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)
