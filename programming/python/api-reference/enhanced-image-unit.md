---
layout: default-layout
title: EnhancedImageUnit Class
description: This page shows EnhancedImageUnit class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_enhanced_image, set_enhanced_image, EnhancedImageUnit, api reference
---

# EnhancedImageUnit Class

The `EnhancedImageUnit` class represents an intermediate result unit whose type is enhanced images.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class EnhancedImageUnit(IntermediateResultUnit):
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> EnhancedImageUnit

## Methods

| Method | Description |
|--------|-------------|
| [`get_enhanced_image`](#get_enhanced_image) | Gets an `EnhancedImageElement` object from current object. |
| [`set_enhanced_image`](#set_enhanced_image) | Sets the enhanced image. |

### get_enhanced_image

Gets an `EnhancedImageElement` object from current unit.

```python
def get_enhanced_image(self) -> EnhancedImageElement:
```

**Return Value**

Returns the `EnhancedImageElement` object.

**See Also**

* [EnhancedImageElement]({{ site.ddn_python_api }}enhanced-image-element.html)

### set_enhanced_image

Sets the enhanced image.

```python
def set_enhanced_image(self, element: EnhancedImageElement) -> int: 
```

**Parameters**

`element` The enhanced image to be set.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [EnhancedImageElement]({{ site.ddn_python_api }}enhanced-image-element.html)
