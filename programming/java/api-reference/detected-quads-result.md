---
layout: default-layout
title: DetectedQuadsResult Class - Dynamsoft Document Normalizer Module Java Edition API Reference
description: Definition of DetectedQuadsResult class in Dynamsoft Document Normalizer Module Java Edition.
keywords: getItems, getErrorCode, getErrorString, getOriginalImageHashId, getOriginalImageTag, DetectedQuadsResult, api reference
---

# DetectedQuadsResult Class

The `DetectedQuadsResult` class stores a captured result whose type is detected quads.

## Definition

*Package:* com.dynamsoft.ddn

```java
public class DetectedQuadsResult
```

## Methods

| Method | Description |
|--------|-------------|
| [`getErrorCode`](#geterrorcode) | Gets the error code of the detection operation. |
| [`getErrorString`](#geterrorstring) | Gets the error message of the detection operation. |
| [`getItems`](#getitems) | Gets the detected quadrilateral item at a specified index. |
| [`getRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image. |

### getErrorCode

Gets the error code of the detection operation.

```java
public int getErrorCode()
```

**Return Value**

Returns the error code.

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)

### getErrorString

Gets the error message of the detection operation.

```java
public String getErrorString()
```

**Return Value**

Returns a string that represents the error message.

### getItems

Gets all the detected quadrilateral items.

```java
public DetectedQuadResultItem[] getItems()
```

**Return Value**

Returns a `DetectedQuadResultItem` array.

**See Also**

[DetectedQuadResultItem]({{ site.ddn_java_api }}detected-quad-result-item.html)

### getRotationTransformMatrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```java
public double[] getRotationTransformMatrix()
```

**Return Value**

Returns a double array of length 9 which represents a 3x3 rotation matrix.

### getOriginalImageHashId

Gets the hash ID of the original image.

```java
public String getOriginalImageHashId()
```

**Return Value**

Returns a string that represents the hash ID of the original image.

### getOriginalImageTag

Gets the tag of the original image.

```java
public ImageTag getOriginalImageTag()
```

**Return Value**

Returns an `ImageTag` object that represents the tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_java_api }}core/basic-classes/image-tag.html)

