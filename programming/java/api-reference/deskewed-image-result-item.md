---
layout: default-layout
title: DeskewedImageResultItem Class
description: This page shows DeskewedImageResultItem class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: getImageData, getSourceDeskewQuad, getCrossVerificationStatus, getOriginalToLocalMatrix, DeskewedImageResultItem, api reference
---

# DeskewedImageResultItem Class

The `DeskewedImageResultItem` class stores a captured result item whose type is Deskewed image.

## Definition

*Package:* com.dynamsoft.ddn

```java
public class DeskewedImageResultItem extends CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcvb_java_api }}core/basic-classes/captured-result-item.html) -> DeskewedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`getImageData`](#getimagedata) | Gets the ImageData of current object. |
| [`getSourceDeskewQuad`](#getsourcedeskewquad)| Gets the quadrilateral used for deskewing the image. |
| [`getCrossVerificationStatus`](#getcrossverificationstatus)| Gets the status of current object as a verified deskewed image. |
| [`getOriginalToLocalMatrix`](#getoriginaltolocalmatrix) | Gets the transformation matrix from the original image coordinate system to the local coordinate system. |

### getImageData

Gets the ImageData of current object.

```java
public ImageData getImageData()
```

**Return Value**

The image data.

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

### getCrossVerificationStatus

Gets the status of current object as a verified deskewed image.

```java
public @EnumCrossVerificationStatus int getCrossVerificationStatus()
```

**Return Value**

Return the status of current object as a verified deskewed image.

**See Also**

[EnumCrossVerificationStatus]({{ site.dcvb_java_api }}core/enum-cross-verification-status.html)

### getOriginalToLocalMatrix

Gets the transformation matrix from the original image coordinate system to the local coordinate system.

```java
public double[] getOriginalToLocalMatrix()
```

**Return Value**

A double array of size 9, representing the 3x3 transformation matrix that converts coordinates from the original image to the local image.