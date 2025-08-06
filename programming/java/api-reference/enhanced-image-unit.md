---
layout: default-layout
title: EnhancedImageUnit Class - Dynamsoft Document Normalizer Module Java Edition API Reference
description: Definition of the EnhancedImageUnit class in Dynamsoft Document Normalizer Module Java Edition.
keywords: getEnhancedImage, setEnhancedImage, EnhancedImageUnit, api reference, java
---

# EnhancedImageUnit

The `EnhancedImageUnit` class represents an intermediate result unit whose type is enhanced images.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> EnhancedImageUnit

```java
public class EnhancedImageUnit extends IntermediateResultUnit
```

## Methods

| Method | Description |
|--------|-------------|
| [`getEnhancedImage`](#getenhancedimage) | Gets an `EnhancedImageElement` object from current object. |
| [`setEnhancedImage`](#setenhancedimage) | Sets the enhanced image. |

### getEnhancedImage

Gets an `EnhancedImageElement` object from current unit.

```java
public EnhancedImageElement getEnhancedImage()
```

**Return Value**

Returns the `EnhancedImageElement` object.

**See Also**

* [EnhancedImageElement]({{ site.ddn_java_api }}enhanced-image-element.html)

### setEnhancedImage

Sets the enhanced image.

```java
public void setEnhancedImage(EnhancedImageElement element) throws DocumentNormalizerException
```

**Parameters**

`element` The enhanced image to be set.

**Exceptions**

[`DocumentNormalizerException`]({{ site.ddn_java_api }}document-normalizer-exception.html)

**See Also**

* [EnhancedImageElement]({{ site.ddn_java_api }}enhanced-image-element.html)
