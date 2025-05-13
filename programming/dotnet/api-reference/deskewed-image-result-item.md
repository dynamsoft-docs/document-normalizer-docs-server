---
layout: default-layout
title: DeskewedImageResultItem Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows DeskewedImageResultItem class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetImageData, SaveToFile, DeskewedImageResultItem, api reference
---

# DeskewedImageResultItem Class

The `DeskewedImageResultItem` class stores a captured result item whose type is Deskewed image.

## Definition

*Namespace:* Dynamsoft.DDN


```csharp
class DeskewedImageResultItem : CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-item.html) -> DeskewedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetImageData`](#getimagedata) | Gets the `ImageData` of current object. |
| [`GetSourceDeskewQuad`](#getsourcedeskewquad)| Gets the quadrilateral used for deskewing the image. |
| [`GetCrossVerificationStatus`](getcrossverificationstatus)| Gets the status of current object as a verified deskewed image. |
| [`GetOriginalToLocalMatrix`](getoriginaltolocalmatrix) | Gets the transformation matrix from the original image coordinate system to the local coordinate system. |

### GetImageData

Gets the `ImageData` of current object.

```csharp
ImageData GetImageData() 
```

**Return Value**

The image data.

**See Also**

* [ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### GetSourceDeskewQuad

Gets the quadrilateral used for deskewing the image.

```csharp
Quadrilateral GetSourceDeskewQuad()
```

**Return Value**

A `Quadrilateral` object representing the four corners of the quadrilateral used to deskew the image.

**See Also**

* [Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### GetCrossVerificationStatus

Gets the status of current object as a verified deskewed image.

```csharp
EnumCrossVerificationStatus GetCrossVerificationStatus()
```

**Return Value**

Return a value from `EnumCrossVerificationStatus` representing the status of the deskewed image result.

**See Also**

* [EnumCrossVerificationStatus]({{ site.dcvb_dotnet_api }}core/cross-verification-status.html)

### GetOriginalToLocalMatrix

Gets the transformation matrix from the original image coordinate system to the local coordinate system.

```csharp
double[] GetOriginalToLocalMatrix()
```

**Return Value**

Returns a double array of size 9, representing the 3x3 transformation matrix that converts coordinates from the original image to the local image.
