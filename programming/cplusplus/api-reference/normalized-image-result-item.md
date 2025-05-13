---
layout: default-layout
title: CNormalizedImageResultItem Class
description: This page shows CNormalizedImageResultItem class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetImageData, SaveToFile, CNormalizedImageResultItem, api reference
---

# CNormalizedImageResultItem Class

The `CNormalizedImageResultItem` class stores a captured result item whose type is normalized image.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CNormalizedImageResultItem: CCapturedResultItem
```

*Inheritance:* [CCapturedResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html) -> CNormalizedImageResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetImageData`](#getimagedata) | Gets the ImageData of current object. |
| [`GetLocation`](#getlocation) | Get the quadrilateral from which you get the normalized image result item. |
| [`GetCrossVerificationStatus`](#getcrossverificationstatus) | Gets the status of current object as a verified normalized image. |

### GetImageData

Gets the ImageData of current object.

```cpp
const CImageData* GetImageData() 
```

**Return Value**

The image data.

**See Also**

* [CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### GetLocation

Gets the location of current object.

```cpp
const CQuadrilateral GetLocation() 
```

**Return Value**

The location of current object.

**See Also**

* [CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

### GetCrossVerificationStatus

Gets the status of current object as a verified normalized image.

```cpp
virtual CrossVerificationStatus GetCrossVerificationStatus() const = 0
```

**Return Value**

The `CrossVerificationStatus` of the normalized image result.

**See Also**

* [CrossVerificationStatus]({{ site.dcvb_enumerations }}core/cross-verification-status.html?lang=cpp)
