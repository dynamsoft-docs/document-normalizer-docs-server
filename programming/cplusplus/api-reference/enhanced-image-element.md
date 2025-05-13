---
layout: default-layout
title: CEnhancedImageElement Class
description: This page shows CEnhancedImageElement class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: SetImageData, CEnhancedImageElement, api reference
---

# CEnhancedImageElement Class

The `CEnhancedImageElement` class stores an intermediate result whose type is Enhanced image.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CEnhancedImageElement: public CRegionObjectElement
```

*Inheritance:* [CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html) -> CEnhancedImageElement

## Methods

| Method | Description |
|--------|-------------|
| [`SetImageData`](#setimagedata) | Sets the image data of the Enhanced image element. |

### SetImageData

Sets the image data of the Enhanced image element.

```cpp
virtual int SetImageData(const CImageData* imgData) = 0;
```

**Parameters**

`imgData`  The image data to set.

**Return Value**

Returns 0 if succeeds, nonzero otherwise. 

**See Also**

* [CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)