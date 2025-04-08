---
layout: default-layout
title: DetectedQuadsUnit Class
description: This page shows DetectedQuadsUnit class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_count, get_detected_quad, DetectedQuadsUnit, api reference
---

# DetectedQuadsUnit Class

The `DetectedQuadsUnit` class represents an intermediate result unit whose type is detected quads.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class DetectedQuadsUnit(IntermediateResultUnit)
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> DetectedQuadsUnit

## Methods

| Method | Description |
|--------|-------------|
| [`get_count`](#get_count) | Gets the count of `DetectedQuadElement` objects in current object.|
| [`get_detected_quad`](#get_detected_quad) | Gets a `DetectedQuadElement` object from current object by specifying a index. |
| [`remove_all_detected_quads`](#remove_all_detected_quads) | Removes all the detected quads in current object. |
| [`remove_detected_quad`](#remove_detected_quad) | Removes a detected quad from current object by specifying an index. |
| [`add_detected_quad`](#add_detected_quad) | Adds a detected quad to current object. |
| [`set_detected_quad`](#set_detected_quad) | Sets the detected quad at the specified index. |

### get_count

Gets the count of `DetectedQuadElement` objects in current object.

```python
def get_count(self) -> int:
```

**Return Value**

The count of `DetectedQuadElement` objects in current object.

### get_detected_quad

Gets a `DetectedQuadElement` object from current object by specifying a index.

```python
def get_detected_quad(self, index: int) -> DetectedQuadElement:
```

**Parameters**

`index` The index of the `DetectedQuadElement` object.

**Return Value**

Returns the `DetectedQuadElement` object got by the specific index.

**See Also**

[DetectedQuadElement]({{ site.ddn_python_api }}detected-quad-element.html)

### remove_all_detected_quads

Removes all the DetectedQuads in current object.

```python
def remove_all_detected_quads(self) -> None:
```

### remove_detected_quad

Removes a detected quad from current object by specifying an index.

```python
def remove_detected_quad(self, index: int) -> int:
```

**Parameters**

`index` The index of the detected quad to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### add_detected_quad

Adds a `DetectedQuadElement` object to current object.

```python
def add_detected_quad(self, element: DetectedQuadElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`element` The detected quad to be added.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[DetectedQuadElement]({{ site.ddn_python_api }}detected-quad-element.html)

### set_detected_quad

Sets the DetectedQuad at the specified index.

```python
def set_detected_quad(self, index: int, element: DetectedQuadElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the detected quad to be set.

`element` The detected quad to be added.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[DetectedQuadElement]({{ site.ddn_python_api }}detected-quad-element.html)
