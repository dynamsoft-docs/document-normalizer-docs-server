---
layout: default-layout
title: CNormalizedImageResultItem Class
description: This page shows CNormalizedImageResultItem class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetImageData, SaveToFile, CNormalizedImageResultItem, api reference
permalink: /programming/cplusplus/api-reference/normalized-image-result-item-v2.4.2000.html
---

# CNormalizedImageResultItem Class

The CNormalizedImageResultItem class stores a captured result item whose type is normalized image.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CNormalizedImageResultItem: CCapturedResultItem
```

*Inheritance:* [CCapturedResultItem]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html) -> CNormalizedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetImageData`](#getimagedata) | Gets the ImageData of current object. |
| [`GetLocation`](#getlocation) | Get the quadrilateral from which you get the normalized image result item. |

### GetImageData

Gets the ImageData of current object.

```cpp
const CImageData* GetImageData() 
```

**Return Value**

The image data.

**See Also**

* [CImageData]({{ site.dcv_cpp_api }}core/basic-structures/image-data.html)

### GetLocation

Gets the location of current object.

```cpp
const CQuadrilateral GetLocation() 
```

**Return Value**

The location of current object.

**See Also**

* [CQuadrilateral]({{ site.dcv_cpp_api }}core/basic-structures/quadrilateral.html)

