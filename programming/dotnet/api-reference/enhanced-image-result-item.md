---
layout: default-layout
title: EnhancedImageResultItem Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows EnhancedImageResultItem class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetImageData, SaveToFile, EnhancedImageResultItem, api reference
---

# EnhancedImageResultItem Class

The `EnhancedImageResultItem` class stores a captured result item whose type is Enhanced image.

## Definition

*Namespace:* Dynamsoft.DDN


```csharp
class EnhancedImageResultItem : CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-item.html) -> EnhancedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetImageData`](#getimagedata) | Gets the ImageData of current object. |
| [`GetOriginalToLocalMatrix`](getoriginaltolocalmatrix) | Gets the transformation matrix from the original image coordinate system to the local coordinate system. |

### GetImageData

Gets the ImageData of current object.

```csharp
ImageData GetImageData() 
```

**Return Value**

The image data.

**See Also**

* [ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### GetOriginalToLocalMatrix

Gets the transformation matrix from the original image coordinate system to the local coordinate system.

```csharp
double[] GetOriginalToLocalMatrix()
```

**Return Value**

Returns a double array of size 9, representing the 3x3 transformation matrix that converts coordinates from the original image to the local image.
