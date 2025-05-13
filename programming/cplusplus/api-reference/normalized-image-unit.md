---
layout: default-layout
title: CNormalizedImagesUnit Class
description: This page shows CNormalizedImagesUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetNormalizedImage, CNormalizedImagesUnit, api reference
permalink: /programming/cplusplus/api-reference/normalized-image-unit.html
---

# CNormalizedImagesUnit Class

The `CNormalizedImagesUnit` class represents an intermediate result unit whose type is normalized images.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CNormalizedImagesUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CNormalizedImagesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of `CNormalizedImageElement` objects in current object. |
| [`GetNormalizedImage`](#getnormalizedimage) | Gets a NormalizedImage object from current object. |
| [`operator[]`](#operator) | Gets a NormalizedImage object from current object by specifying a index. |
| [`RemoveAllNormalizedImages`](#removeallnormalizedimages) | Removes all the normalized images in current object. |
| [`SetNormalizedImage`](#setnormalizedimage) | Sets the normalized image. |

### GetCount

Gets the count of `CNormalizedImageElement` objects in current object.

```cpp
int GetCount() 
```

**Return Value**

The count of `CNormalizedImageElement` objects in current object.

### GetNormalizedImage

Gets a NormalizedImage object from current object.

```cpp
const CNormalizedImageElement* GetNormalizedImage(int index)
```

**Return Value**

Returns the NormalizedImage object.

**See Also**

* [CNormalizedImageElement]({{cpp_api}}normalized-image-element.html)

### operator[]

Gets a NormalizedImage object from current object by specifying a index.

```cpp
virtual const CNormalizedImageElement* operator[](int index) const = 0
```

**Parameters**

`[in] index` The index of the desired CNormalizedImageElement object.

**Return value**

Returns a pointer to the CNormalizedImageElement object at the specified index.

### RemoveAllNormalizedImages

Removes all the normalized images in current object.

```cpp
virtual void RemoveAllNormalizedImages() = 0
```

### SetNormalizedImage

Sets the normalized image.

```cpp
virtual int SetNormalizedImage(const CNormalizedImageElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0
```

**Parameters**

`[in] element` The normalized image to be set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.