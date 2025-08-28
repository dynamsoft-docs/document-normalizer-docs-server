---
layout: default-layout
title: LongLinesUnit Class
description: This page shows LongLinesUnit class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: getCount, getLongLine, LongLinesUnit, api reference
---

# LongLinesUnit Class

The `LongLinesUnit` class represents an intermediate result unit whose type is long lines. Short line segments that are located in the same line are extended and merged to form a long line segment.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

```java
public class LongLinesUnit extends IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> LongLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`getCount`](#getcount) | Gets the count of `LineSegment` objects in current object.|
| [`getLongLine`](#getlongline) | Gets a `LineSegment` object from current object by specifying a index. |
| [`getLongLines`](#getlonglines) | Gets all `LineSegment` objects in current object. |
| [`removeAllLongLines`](#removealllonglines) | Removes all the `LongLines` in current object. |
| [`removeLongLine`](#removelongline) | Removes a `LongLine` from current object by specifying an index. |
| [`addLongLine`](#addlongline) | Adds a `LongLine` to current object. |
| [`setLongLine`](#setlongline) | Sets the `LongLine` at the specified index. |

### getCount

Gets the count of `LineSegment` objects in current object.

```java
public int getCount()
```

**Return Value**

The count of `LineSegment` objects in current object.

### getLongLine

Gets a `LineSegment` object from current object by specifying a index.

```java
public LineSegment getLongLine(int index)
```

**Parameters**

`index` The index of the `LineSegment` object.

**Return Value**

Returns the `LineSegment` object.

**See Also**

* [LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

### getLongLines

Gets all `LineSegment` objects in current object.

```java
public LineSegment[] getLongLines()
```

**Return Value**

Returns an array of `LineSegment` objects.

**See Also**

* [LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

### removeAllLongLines

Removes all the `LongLines` in current object.

```java
public void removeAllLongLines()
```

### removeLongLine

Removes a `LongLine` from current object by specifying an index.

```java
public void removeLongLine(int index) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the `LongLine` to be removed.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.md)

### addLongLine

Adds a `LongLine` to current object.

```java
public void addLongLine(LineSegment line) throws DocumentNormalizerException
public void addLongLine(LineSegment line, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`line` The `LongLine` to be added.

`matrixToOriginalImage` The matrix to the original image.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.md)

**See Also**

* [LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

### setLongLine

Sets the `LongLine` at the specified index.

```java
public void setLongLine(int index, LineSegment line) throws DocumentNormalizerException
public void setLongLine(int index, LineSegment line, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the `LongLine` to be set.

`line` the `LongLine` to be set.

`matrixToOriginalImage` The matrix to the original image.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.md)
