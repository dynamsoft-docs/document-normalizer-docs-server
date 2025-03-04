---
layout: default-layout
title: CDeskewedImagesUnit Class
description: This page shows CDeskewedImagesUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetDeskewedImage, CDeskewedImagesUnit, api reference
permalink: /programming/cplusplus/api-reference/Deskewed-image-unit.html
---

# CDeskewedImagesUnit Class

The CDeskewedImagesUnit class represents an intermediate result unit whose type is Deskewed images.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDeskewedImagesUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CDeskewedImagesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetDeskewedImage`](#getdeskewedimage) | Gets a DeskewedImage object from current object. |
| [`SetDeskewedImage`](#setdeskewedimage) | Sets the Deskewed image. |

### GetDeskewedImage

Gets a DeskewedImage object from current unit.

```cpp
virtual const CDeskewedImageElement* GetDeskewedImage() const = 0;
```

**Return Value**

Returns the `CDeskewedImageElement` object.

**See Also**

* [CDeskewedImageElement]({{ site.ddn_cpp_api }}deskewed-image-element.html)

### SetDeskewedImage

Sets the Deskewed image.

```cpp
virtual int SetDeskewedImage(const CDeskewedImageElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] element` The Deskewed image to be set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.