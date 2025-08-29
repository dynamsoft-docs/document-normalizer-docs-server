---
layout: default-layout
title: DeskewedImageElement Class
description: This page shows DeskewedImageElement class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: setImageData, getSourceDeskewQuad, DeskewedImageElement, api reference
---

# DeskewedImageElement Class

The `DeskewedImageElement` class stores an intermediate result whose type is Deskewed image.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

```java
public class DeskewedImageElement extends RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html) -> DeskewedImageElement

## Methods

| Method | Description |
|--------|-------------|
| [`DeskewedImageElement`](#deskewedimageelement) | Initializes a new instance of the `DeskewedImageElement` class. |
| [`setImageData`](#setimagedata) | Sets the image data of the deskewed image element. |
| [`getSourceDeskewQuad`](#getsourcedeskewquad) | Gets the quadrilateral used for deskewing the image. |

### DeskewedImageElement

Initializes a new instance of the `DeskewedImageElement` class.

```java
public DeskewedImageElement()
```

### setImageData

Sets the image data of the deskewed image element.

```java
public void setImageData(ImageData imageData) throws DocumentNormalizerException
```

**Parameters**

`imageData`  The image data to set.

**Exceptions**

[`DocumentNormalizerException`]({{ site.ddn_java_api }}document-normalizer-exception.html)

**See Also**

* [ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### getSourceDeskewQuad

Gets the quadrilateral used for deskewing the image.

```java
public Quadrilateral getSourceDeskewQuad()
```

**Return Value**

A `Quadrilateral` object representing the four corners of the quadrilateral used to deskew the image.

**See Also**

* [Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

