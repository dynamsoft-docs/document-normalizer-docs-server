---
layout: default-layout
title: EnhancedImageElement Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows EnhancedImageElement class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: SetImageData, EnhancedImageElement, api reference
---

# EnhancedImageElement Class

The `EnhancedImageElement` class stores an intermediate result whose type is Enhanced image.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class EnhancedImageElement : RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html) -> EnhancedImageElement

## Methods

| Method | Description |
|--------|-------------|
| [`SetImageData`](#setimagedata) | Sets the image data of the Enhanced image element. |

### SetImageData

Sets the image data of the Enhanced image element.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`imgData`  The image data to set.

**Return Value**

Returns 0 if succeeds, nonzero otherwise. 

**See Also**

* [ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)