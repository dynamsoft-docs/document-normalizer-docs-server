---
layout: default-layout
title: CEnhancedImagesUnit Class
description: This page shows CEnhancedImagesUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetEnhancedImage, CEnhancedImagesUnit, api reference
---

# CEnhancedImagesUnit Class

The CEnhancedImagesUnit class represents an intermediate result unit whose type is enhanced images.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CEnhancedImagesUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CEnhancedImagesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetEnhancedImage`](#getenhancedimage) | Gets a enhancedImage object from current object. |
| [`SetEnhancedImage`](#setenhancedimage) | Sets the enhanced image. |

### GetEnhancedImage

Gets a enhancedImage object from current unit.

```cpp
virtual const CEnhancedImageElement* GetEnhancedImage() const = 0;
```

**Return Value**

Returns the `CEnhancedImageElement` object.

**See Also**

* [CEnhancedImageElement]({{ site.ddn_cpp_api }}enhanced-image-element.html)

### SetEnhancedImage

Sets the enhanced image.

```cpp
virtual int SetEnhancedImage(const CEnhancedImageElement* element) = 0;  
```

**Parameters**

`[in] element` The enhanced image to be set.

**Return value**

Returns 0 if successful, otherwise returns a negative value.