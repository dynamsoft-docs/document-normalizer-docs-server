---
layout: default-layout
title: NormalizedImagesUnit Class
description: This page shows NormalizedImagesUnit class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_normalized_image, NormalizedImagesUnit, api reference
---

# NormalizedImagesUnit Class

The `NormalizedImagesUnit` class represents an intermediate result unit whose type is normalized images.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class NormalizedImagesUnit(IntermediateResultUnit)
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> NormalizedImagesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`get_count`](#get_count) | Gets the count of `NormalizedImageElement` objects in current object. |
| [`get_normalized_image`](#get_normalized_image) | Gets a `NormalizedImageElement` object from current object. |
| [`operator[]`](#operator) | Gets a `NormalizedImageElement` object from current object by specifying a index. |
| [`remove_all_normalized_images`](#remove_all_normalized_images) | Removes all the normalized images in current object. |
| [`set_normalized_image`](#set_normalized_image) | Sets the normalized image. |

### get_count

Gets the count of `NormalizedImageElement` objects in current object.

```python
def get_count(self) -> int:
```

**Return Value**

The count of `NormalizedImageElement` objects in current object.

### get_normalized_image

Gets a `NormalizedImageElement` object from current object.

```python
def get_normalized_image(self, index: int) -> NormalizedImageElement:
```

**Parameters**

`index` The index of the `NormalizedImageElement` object.

**Return Value**

Returns the `NormalizedImageElement` object.

**See Also**

[NormalizedImageElement]({{ site.ddn_python_api }}normalized-image-element.html)

### remove_all_normalized_images

Removes all the normalized images in current object.

```python
def remove_all_normalized_images(self) -> None:
```

### set_normalized_image

Sets the normalized image.

```python
def set_normalized_image(self, element: NormalizedImageElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`element` The normalized image to be set.

`matrix_to_original_image` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[NormalizedImageElement]({{ site.ddn_python_api }}normalized-image-element.html)
