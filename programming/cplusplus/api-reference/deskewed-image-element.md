---
layout: default-layout
title: CDeskewedImageElement Class
description: This page shows CDeskewedImageElement class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetImageData, CDeskewedImageElement, api reference
---

# CDeskewedImageElement Class

The `CDeskewedImageElement` class stores an intermediate result whose type is Deskewed image.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDeskewedImageElement: public CRegionObjectElement
```

*Inheritance:* [CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html) -> CDeskewedImageElement

## Methods

| Method | Description |
|--------|-------------|
| [`SetImageData`](#setimagedata) | Sets the image data of the deskewed image element. |
| [`GetSourceDeskewQuad`](#getsourcedeskewquad) | Gets the quadrilateral used for deskewing the image. |

### SetImageData

Sets the image data of the deskewed image element.

```cpp
virtual int SetImageData(const CImageData* imgData) = 0;
```

**Parameters**

`imgData`  The image data to set.

**Return Value**

Returns 0 if succeeds, nonzero otherwise. 

**See Also**

* [CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### GetSourceDeskewQuad

Gets the quadrilateral used for deskewing the image.

```cpp
virtual CQuadrilateral GetSourceDeskewQuad() const = 0;
```

**Return Value**

Returns A `CQuadrilateral` object representing the four corners of the quadrilateral used to deskew the image.
