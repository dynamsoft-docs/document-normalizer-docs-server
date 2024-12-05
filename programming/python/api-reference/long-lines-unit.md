---
layout: default-layout
title: LongLinesUnit Class
description: This page shows LongLinesUnit class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_count, get_long_line, LongLinesUnit, api reference
---

# LongLinesUnit Class

The `LongLinesUnit` class represents an intermediate result unit whose type is long lines. Short line segments that are located in the same line are extended and merged to form a long line segment.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class LongLinesUnit(IntermediateResultUnit)
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> LongLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`get_count`](#get_count) | Gets the count of `LongLine` objects in current object.|
| [`get_long_line`](#get_long_line) | Gets a `LongLine` object from current object by specifying a index. |
| [`remove_all_long_lines`](#remove_all_long_lines) | Removes all the `LongLines` in current object. |
| [`remove_long_line`](#remove_long_line) | Removes a `LongLine` from current object by specifying an index. |
| [`add_long_line`](#add_long_line) | Adds a `LongLine` to current object. |
| [`set_long_line`](#set_long_line) | Sets the `LongLine` at the specified index. |

### get_count

Gets the count of `LongLine` objects in current object.

```python
def get_count(self) -> int:
```

**Return Value**

The count of `LongLine` objects in current object.

### get_long_line

Gets a `LongLine` object from current object by specifying a index.

```python
def get_long_line(self, index: int) -> LineSegment:
```

**Parameters**

`index` The index of the `LongLine` object.

**Return Value**

Returns the `LongLine` object.

**See Also**

* [LineSegment]({{ site.dcv_python_api }}core/basic-classes/line-segment.html)

### remove_all_long_lines

Removes all the `LongLines` in current object.

```python
def remove_all_long_lines(self) -> None:
```

### remove_long_line

Removes a `LongLine` from current object by specifying an index.

```python
def remove_long_line(self, index: int) -> int:
```

**Parameters**

`index` The index of the `LongLine` to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### add_long_line

Adds a `LongLine` to current object.

```python
def add_long_line(self, line: LineSegment, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`line` The `LongLine` to be added.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [LineSegment]({{ site.dcv_python_api }}core/basic-classes/line-segment.html)

### set_long_line

Sets the `LongLine` at the specified index.

```python
def set_long_line(self, index: int, line: LineSegment, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the `LongLine` to be set.

`line` the `LongLine` to be set.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.
