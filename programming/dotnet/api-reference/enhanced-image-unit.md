---
layout: default-layout
title: EnhancedImagesUnit Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows EnhancedImagesUnit class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetEnhancedImage, EnhancedImagesUnit, api reference
---

# EnhancedImagesUnit Class

The `EnhancedImagesUnit` class represents an intermediate result unit whose type is enhanced images.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class EnhancedImagesUnit: IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> EnhancedImagesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetEnhancedImage`](#getenhancedimage) | Gets an `EnhancedImageElement` object from current object. |
| [`SetEnhancedImage`](#setenhancedimage) | Sets the enhanced image. |

### GetEnhancedImage

Gets an `EnhancedImageElement` object from current unit.

```csharp
EnhancedImageElement GetEnhancedImage()
```

**Return Value**

Returns the `EnhancedImageElement` object.

**See Also**

* [EnhancedImageElement]({{ site.ddn_dotnet_api }}enhanced-image-element.html)

### SetEnhancedImage

Sets the enhanced image.

```csharp
int SetEnhancedImage(EnhancedImageElement enhancedImage)  
```

**Parameters**

`[in] enhancedImage` The enhanced image to be set.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [EnhancedImageElement]({{ site.ddn_dotnet_api }}enhanced-image-element.html)
