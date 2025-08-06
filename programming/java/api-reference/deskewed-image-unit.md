---
layout: default-layout
title: DeskewedImageUnit Class
description: This page shows DeskewedImageUnit class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: getDeskewedImage, setDeskewedImage, DeskewedImageUnit, api reference
---

# DeskewedImageUnit Class

The `DeskewedImageUnit` class represents an intermediate result unit whose type is Deskewed images.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

```java
public class DeskewedImageUnit extends IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> DeskewedImageUnit

## Methods

| Method | Description |
|--------|-------------|
| [`getDeskewedImage`](#getdeskewedimage) | Gets a `DeskewedImageElement` object from current object. |
| [`setDeskewedImage`](#setdeskewedimage) | Sets the deskewed image. |

### getDeskewedImage

Gets a `DeskewedImageElement` object from current unit.

```java
public DeskewedImageElement getDeskewedImage()
```

**Return Value**

Returns the `DeskewedImageElement` object.

**See Also**

* [DeskewedImageElement]({{ site.ddn_java_api }}deskewed-image-element.html)

### setDeskewedImage

Sets the deskewed image.

```java
public void setDeskewedImage(DeskewedImageElement element) throws DocumentNormalizerException
public void setDeskewedImage(DeskewedImageElement element, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`element` The deskewed image to be set.

`matrixToOriginalImage` The matrix to original image.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.html)

**See Also**

* [DeskewedImageElement]({{ site.ddn_java_api }}deskewed-image-element.html)
