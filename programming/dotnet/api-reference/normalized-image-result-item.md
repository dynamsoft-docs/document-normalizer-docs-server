---
layout: default-layout
title: NormalizedImageResultItem Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: Definition of NormalizedImageResultItem class in Dynamsoft Document Normalizer Module .NET Edition.
keywords: GetImageData, SaveToFile, NormalizedImageResultItem, api reference
---

# NormalizedImageResultItem Class

The NormalizedImageResultItem class stores a captured result item whose type is normalized image.

## Definition

*Namespace:* Dynamsoft.DDN

*Assembly:* Dynamsoft.DocumentNormalizer.dll

```csharp
public class NormalizedImageResultItem: CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcv_dotnet_api }}core/basic-classes/captured-result-item.html) -> NormalizedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetImageData`](#getimagedata) | Gets the ImageData of current object. |
| [`GetLocation`](#getlocation) | Get the quadrilateral from which you get the normalized image result item. |
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Get the rotation transformation matrix. |

### GetImageData

Gets the ImageData of current object.

```csharp
ImageData GetImageData() 
```

**Return Value**

The image data.

**See Also**

* [ImageData]({{ site.dcv_dotnet_api }}core/basic-classes/image-data.html)

### GetLocation

Gets the location of current object.

```csharp
const Quadrilateral GetLocation() 
```

**Return Value**

The location of current object.

**See Also**

* [Quadrilateral]({{ site.dcv_dotnet_api }}core/basic-classes/quadrilateral.html)

### GetRotationTransformMatrix

Get the rotation transformation matrix.

```csharp
double[] GetRotationTransformMatrix()
```
