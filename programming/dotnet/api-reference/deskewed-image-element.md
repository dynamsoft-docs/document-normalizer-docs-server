---
layout: default-layout
title: DeskewedImageElement Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows DeskewedImageElement class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetImageData, DeskewedImageElement, api reference
---

# DeskewedImageElement Class

The `DeskewedImageElement` class stores an intermediate result whose type is Deskewed image.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class DeskewedImageElement : RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html) -> DeskewedImageElement

## Methods

| Method | Description |
|--------|-------------|
| [`SetImageData`](#setimagedata) | Sets the image data of the deskewed image element. |
| [`GetSourceDeskewQuad`](#getsourcedeskewquad) | Gets the quadrilateral used for deskewing the image. |

### SetImageData

Sets the image data of the deskewed image element.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`imgData`  The image data to set.

**Return Value**

Returns 0 if succeeds, nonzero otherwise. 

**See Also**

* [ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### GetSourceDeskewQuad

Gets the quadrilateral used for deskewing the image.

```csharp
Quadrilateral GetSourceDeskewQuad()
```

**Return Value**

Returns A `Quadrilateral` object representing the four corners of the quadrilateral used to deskew the image.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)
