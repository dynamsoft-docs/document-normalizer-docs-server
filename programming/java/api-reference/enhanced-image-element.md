---
layout: default-layout
title: EnhancedImageElement Class
description: This page shows EnhancedImageElement class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: setImageData, EnhancedImageElement, api reference
---

# EnhancedImageElement Class

The `EnhancedImageElement` class stores an intermediate result whose type is Enhanced image.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

```java
public class EnhancedImageElement extends RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html) -> EnhancedImageElement

## Methods

| Method | Description |
|--------|-------------|
| [`EnhancedImageElement`](#enhancedimageelement) | Initializes a new instance of the `EnhancedImageElement` class. |
| [`setImageData`](#setimagedata) | Sets the image data of the Enhanced image element. |

### EnhancedImageElement

Initializes a new instance of the `EnhancedImageElement` class.

```java
public EnhancedImageElement()
```

### setImageData

Sets the image data of the Enhanced image element.

```java
public void setImageData(ImageData imageData) throws DocumentNormalizerException
```

**Parameters**

`imageData`  The image data to set.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.md)

**See Also**

* [ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)
