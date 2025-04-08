---
layout: default-layout
title: CornersUnit Class
description: This page shows CornersUnit class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_count, get_corner, CornersUnit, api reference
---

# CornersUnit Class

The `CornersUnit` class represents an intermediate result unit whose type is corners.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class CornersUnit(IntermediateResultUnit)
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> CornersUnit

## Methods

| Method | Description |
|--------|-------------|
| [`get_count`](#get_count) | Gets the count of `Corner` objects in current object.|
| [`get_corner`](#get_corner) | Gets a `Corner` object from current object by specifying a index. |
| [`remove_all_corners`](#remove_all_corners) | Removes all the corners in current object. |
| [`remove_corner`](#remove_corner) | Removes a corner from current object by specifying an index. |
| [`add_corner`](#add_corner) | Adds a corner to current object. |
| [`set_corner`](#set_corner) | Sets the corner at the specified index. |

### get_count

Gets the count of `Corner` objects in current object.

```python
def get_count(self) -> int:
```

**Return Value**

The count of `Corner` objects in current object.

### get_corner

Gets a `Corner` object from current object by specifying a index.

```python
def get_corner(self, index: int) -> Tuple[int, Corner]:
```

**Parameters**

`index` The index of the `Corner` object.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `corner` <*Corner*>: The `Corner` object got by the specific index.

**See Also**

[EnumErrorCode]({{ site.dcv_python_api }}core/enum-error-code.html?lang=python)

[Corner]({{ site.dcv_python_api }}core/basic-classes/corner.html)

### remove_all_corners

Removes all the corners in current object.

```python
def remove_all_corners(self) -> None:
```

### remove_corner

Removes a corner from current object by specifying an index.

```python
def remove_corner(self, index: int) -> int:
```

**Parameters**

`index` The index of the corner to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### add_corner

Adds a corner to current object.

```python
def add_corner(self, corner: Corner, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`corner` The corner to be added.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[Corner]({{ site.dcv_python_api }}core/basic-classes/corner.html)

### set_corner

Sets the corner at the specified index.

```python
def set_corner(self, index: int, corner: Corner, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the corner to be set.

`corner` The corner to be added.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[Corner]({{ site.dcv_python_api }}core/basic-classes/corner.html)

