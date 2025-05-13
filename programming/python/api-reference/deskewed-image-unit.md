---
layout: default-layout
title: DeskewedImageUnit Class
description: This page shows DeskewedImageUnit class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_deskewed_image, set_deskewed_image, DeskewedImageUnit, api reference
---

# DeskewedImageUnit Class

The `DeskewedImageUnit` class represents an intermediate result unit whose type is Deskewed images.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class DeskewedImageUnit(IntermediateResultUnit):
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-unit.html) -> DeskewedImageUnit

## Methods

| Method | Description |
|--------|-------------|
| [`get_deskewed_image`](#get_deskewed_image) | Gets a `DeskewedImageElement` object from current object. |
| [`set_deskewed_image`](#set_deskewed_image) | Sets the deskewed image. |

### get_deskewed_image

Gets a `DeskewedImageElement` object from current unit.

```python
def get_deskewed_image(self) -> DeskewedImageElement:
```

**Return Value**

Returns the `DeskewedImageElement` object.

**See Also**

* [DeskewedImageElement]({{ site.ddn_cpp_api }}deskewed-image-element.html)

### set_deskewed_image

Sets the deskewed image.

```python
def set_deskewed_image(self, element: DeskewedImageElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`element` The deskewed image to be set.

`matrix_to_original_image` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [DeskewedImageElement]({{ site.ddn_cpp_api }}deskewed-image-element.html)
