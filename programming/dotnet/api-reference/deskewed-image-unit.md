---
layout: default-layout
title: DeskewedImagesUnit Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows DeskewedImagesUnit class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetDeskewedImage, DeskewedImagesUnit, api reference
---

# DeskewedImagesUnit Class

The `DeskewedImagesUnit` class represents an intermediate result unit whose type is deskewed images.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class DeskewedImagesUnit : IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> DeskewedImagesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetDeskewedImage`](#getdeskewedimage) | Gets a `DeskewedImageElement` object from current object. |
| [`SetDeskewedImage`](#setdeskewedimage) | Sets the Deskewed image. |

### GetDeskewedImage

Gets a `DeskewedImageElement` object from current unit.

```csharp
DeskewedImageElement GetDeskewedImage()
```

**Return Value**

Returns the `DeskewedImageElement` object.

**See Also**

* [DeskewedImageElement]({{ site.ddn_dotnet_api }}deskewed-image-element.html)

### SetDeskewedImage

Sets the deskewed image.

```csharp
int SetDeskewedImage(DeskewedImageElement deskewedImage, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] deskewedImage` The deskewed image to be set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.
