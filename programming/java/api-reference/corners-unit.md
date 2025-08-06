---
layout: default-layout
title: CornersUnit Class
description: This page shows CornersUnit class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: getCount, getCorner, CornersUnit, api reference
---

# CornersUnit Class

The `CornersUnit` class represents an intermediate result unit whose type is corners.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

```java
public class CornersUnit extends IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> CornersUnit

## Methods

| Method | Description |
|--------|-------------|
| [`getCount`](#getcount) | Gets the count of `Corner` objects in current object.|
| [`getCorner`](#getcorner) | Gets a `Corner` object from current object by specifying a index. |
| [`getCorners`](#getcorners) | Gets all `Corner` objects in current object. |
| [`removeAllCorners`](#removeallcorners) | Removes all the corners in current object. |
| [`removeCorner`](#removecorner) | Removes a corner from current object by specifying an index. |
| [`addCorner`](#addcorner) | Adds a corner to current object. |
| [`setCorner`](#setcorner) | Sets the corner at the specified index. |

### getCount

Gets the count of `Corner` objects in current object.

```java
public int getCount()
```

**Return Value**

The count of `Corner` objects in current object.

### getCorner

Gets a `Corner` object from current object by specifying a index.

```java
public Corner getCorner(int index) throws DocumentNormalizerException
```
```

**Parameters**

`index` The index of the `Corner` object.

**Return Value**

Returns the `Corner` object got by the specific index.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.html)

**See Also**

[Corner]({{ site.dcvb_java_api }}core/basic-classes/corner.html)

### getCorners

Gets all `Corner` objects in current object.

```java
public Corner[] getCorners()
```

**Return Value**

Returns an array of `Corner` objects.

**See Also**

[Corner]({{ site.dcvb_java_api }}core/basic-classes/corner.html)

### removeAllCorners

Removes all the corners in current object.

```java
public void removeAllCorners() throws DocumentNormalizerException
```

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.html)

### removeCorner

Removes a corner from current object by specifying an index.

```java
public void removeCorner(int index) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the corner to be removed.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.html)

### addCorner

Adds a corner to current object.

```java
public void addCorner(Corner corner) throws DocumentNormalizerException
public void addCorner(Corner corner, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`corner` The corner to be added.

`matrixToOriginalImage` The matrix to the original image.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.html)

**See Also**

[Corner]({{ site.dcvb_java_api }}core/basic-classes/corner.html)

### setCorner

Sets the corner at the specified index.

```java
public void setCorner(int index, Corner corner) throws DocumentNormalizerException
public void setCorner(int index, Corner corner, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the corner to be set.

`corner` The corner to be added.

`matrixToOriginalImage` The matrix to the original image.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.html)

**See Also**

[Corner]({{ site.dcvb_java_api }}core/basic-classes/corner.html)

