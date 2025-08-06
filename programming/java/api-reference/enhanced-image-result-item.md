---
layout: default-layout
title: EnhancedImageResultItem Class
description: This page shows EnhancedImageResultItem class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: getImageData, getOriginalToLocalMatrix, EnhancedImageResultItem, api reference
---

# EnhancedImageResultItem Class

The `EnhancedImageResultItem` class stores a captured result item whose type is Enhanced image.

## Definition

*Package:* com.dynamsoft.ddn

```java
public class EnhancedImageResultItem extends CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcvb_java_api }}core/basic-classes/captured-result-item.html) -> EnhancedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`getImageData`](#getimagedata) | Gets the ImageData of current object. |
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

### getOriginalToLocalMatrix

Gets the transformation matrix from the original image coordinate system to the local coordinate system.

```java
public double[] getOriginalToLocalMatrix()
```

**Return Value**

A double array of size 9, representing the 3x3 transformation matrix that converts coordinates from the original image to the local image.