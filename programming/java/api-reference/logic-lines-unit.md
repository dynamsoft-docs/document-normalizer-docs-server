---
layout: default-layout
title: LogicLinesUnit Class - Dynamsoft Document Normalizer Module Java Edition API Reference
description: Definition of the LogicLinesUnit class in Dynamsoft Document Normalizer Module Java Edition.
keywords: getCount, getLogicLine, LogicLinesUnit, api reference, java
---

# LogicLinesUnit

The `LogicLinesUnit` class represents an intermediate result unit whose type is logic lines. Logic lines are formed by combining long lines that meet certain conditions.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> LogicLinesUnit

```java
public class LogicLinesUnit extends IntermediateResultUnit
```

## Methods

| Method | Description |
|--------|-------------|
| [`getCount`](#getcount) | Gets the count of `LogicLine` objects in current object.|
| [`getLogicLine`](#getlogicline) | Gets a `LogicLine` object from current object by specifying a index. |
| [`getLogicLines`](#getlogiclines) | Gets all the `LogicLine` objects from current object. |
| [`removeAllLogicLines`](#removealllogiclines) | Removes all the `LogicLines` in current object. |
| [`removeLogicLine`](#removelogicline) | Removes a `LogicLine` from current object by specifying an index. |
| [`addLogicLine`](#addlogicline) | Adds a `LogicLine` to current object. |
| [`setLogicLine`](#setlogicline) | Sets the `LogicLine` at the specified index. |

### getCount

Gets the count of `LogicLine` objects in current object.

```java
public int getCount()
```

**Return Value**

The count of `LogicLine` objects in current object.

### getLogicLine

Gets a `LogicLine` object from current object by specifying a index.

```java
public LineSegment getLogicLine(int index)
```

**Parameters**

`index` The index of the `LogicLine` object.

**Return Value**

Returns the `LogicLine` object.

**See Also**

* [LineSegment]({{ site.dcvb_java_api }}core/basic-structures/line-segment.html)

### getLogicLines

Gets all the `LogicLine` objects from current object.

```java
public LineSegment[] getLogicLines()
```

**Return Value**

Returns all the `LogicLine` objects as an array.

**See Also**

* [LineSegment]({{ site.dcvb_java_api }}core/basic-structures/line-segment.html)

### removeAllLogicLines

Removes all the LogicLines in current object.

```java
public void removeAllLogicLines()
```

### removeLogicLine

Removes a `LogicLine` from current object by specifying an index.

```java
public void removeLogicLine(int index) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the `LogicLine` to be removed.

**Exceptions**

[`DocumentNormalizerException`]({{ site.ddn_java_api }}document-normalizer-exception.html)

### addLogicLine

Adds a `LogicLine` to current object.

```java
public void addLogicLine(LineSegment logicline) throws DocumentNormalizerException
public void addLogicLine(LineSegment logicline, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`logicline` The `LogicLine` to be added.

`matrixToOriginalImage` The matrix to the original image. Must be a double array of length 9.

**Exceptions**

[`DocumentNormalizerException`]({{ site.ddn_java_api }}document-normalizer-exception.html)

### setLogicLine

Sets the `LogicLine` at the specified index.

```java
public void setLogicLine(int index, LineSegment logicline) throws DocumentNormalizerException
public void setLogicLine(int index, LineSegment logicline, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the LogicLine to be set.

`logicline` The LogicLine to be added.

`matrixToOriginalImage` The matrix to the original image. Must be a double array of length 9.

**Exceptions**

[`DocumentNormalizerException`]({{ site.ddn_java_api }}document-normalizer-exception.html)
