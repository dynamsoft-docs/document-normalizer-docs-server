---
layout: default-layout
title: DetectedQuadsUnit Class
description: This page shows DetectedQuadsUnit class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: getCount, getDetectedQuad, DetectedQuadsUnit, api reference
---

# DetectedQuadsUnit Class

The `DetectedQuadsUnit` class represents an intermediate result unit whose type is detected quads.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

```java
public class DetectedQuadsUnit extends IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> DetectedQuadsUnit

## Methods

| Method | Description |
|--------|-------------|
| [`getCount`](#getcount) | Gets the count of `DetectedQuadElement` objects in current object.|
| [`getDetectedQuad`](#getdetectedquad) | Gets a `DetectedQuadElement` object from current object by specifying a index. |
| [`getDetectedQuads`](#getdetectedquads) | Gets all `DetectedQuadElement` objects in current object. |
| [`removeAllDetectedQuads`](#removealldetectedquads) | Removes all the detected quads in current object. |
| [`removeDetectedQuad`](#removedetectedquad) | Removes a detected quad from current object by specifying an index. |
| [`addDetectedQuad`](#adddetectedquad) | Adds a detected quad to current object. |
| [`setDetectedQuad`](#setdetectedquad) | Sets the detected quad at the specified index. |

### getCount

Gets the count of `DetectedQuadElement` objects in current object.

```java
public int getCount()
```

**Return Value**

The count of `DetectedQuadElement` objects in current object.

### getDetectedQuad

Gets a `DetectedQuadElement` object from current object by specifying a index.

```java
public DetectedQuadElement getDetectedQuad(int index)
```

**Parameters**

`index` The index of the `DetectedQuadElement` object.

**Return Value**

Returns the `DetectedQuadElement` object got by the specific index.

**See Also**

[DetectedQuadElement]({{ site.ddn_java_api }}detected-quad-element.html)

### getDetectedQuads

Gets all `DetectedQuadElement` objects in current object.

```java
public DetectedQuadElement[] getDetectedQuads()
```

**Return Value**

Returns an array of `DetectedQuadElement` objects.

**See Also**

[DetectedQuadElement]({{ site.ddn_java_api }}detected-quad-element.html)

### removeAllDetectedQuads

Removes all the DetectedQuads in current object.

```java
public void removeAllDetectedQuads()
```

### removeDetectedQuad

Removes a detected quad from current object by specifying an index.

```java
public void removeDetectedQuad(int index) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the detected quad to be removed.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.html)

### addDetectedQuad

Adds a `DetectedQuadElement` object to current object.

```java
public void addDetectedQuad(DetectedQuadElement element) throws DocumentNormalizerException
public void addDetectedQuad(DetectedQuadElement element, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`element` The detected quad to be added.

`matrixToOriginalImage` The matrix to the original image.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.html)

**See Also**

[DetectedQuadElement]({{ site.ddn_java_api }}detected-quad-element.html)

### setDetectedQuad

Sets the DetectedQuad at the specified index.

```java
public void setDetectedQuad(int index, DetectedQuadElement element) throws DocumentNormalizerException
public void setDetectedQuad(int index, DetectedQuadElement element, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the detected quad to be set.

`element` The detected quad to be added.

`matrixToOriginalImage` The matrix to the original image.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.html)

**See Also**

[DetectedQuadElement]({{ site.ddn_java_api }}detected-quad-element.html)
