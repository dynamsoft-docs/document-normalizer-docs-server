---
layout: default-layout
title: LogicLinesUnit Class
description: This page shows LogicLinesUnit class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_count, get_logic_line, LogicLinesUnit, api reference
---

# LogicLinesUnit Class

The `LogicLinesUnit` class represents an intermediate result unit whose type is logic lines. Logic lines are formed by combining long lines that meet certain conditions.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class LogicLinesUnit(IntermediateResultUnit):
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> LogicLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`get_count`](#get_count) | Gets the count of `LogicLine` objects in current object.|
| [`get_logic_line`](#get_logic_line) | Gets a `LogicLine` object from current object by specifying a index. |
| [`remove_all_logic_lines`](#remove_all_logic_lines) | Removes all the `LogicLines` in current object. |
| [`remove_logic_line`](#remove_logic_line) | Removes a `LogicLine` from current object by specifying an index. |
| [`add_logic_line`](#add_logic_line) | Adds a `LogicLine` to current object. |
| [`set_logic_line`](#set_logic_line) | Sets the `LogicLine` at the specified index. |

### get_count

Gets the count of `LogicLine` objects in current object.

```python
def get_count(self) -> int: 
```

**Return Value**

The count of `LogicLine` objects in current object.

### get_logic_line

Gets a `LogicLine` object from current object by specifying a index.

```python
def get_logic_line(self, index: int) -> LineSegment:
```

**Parameters**

`index` The index of the `LogicLine` object.

**Return Value**

Returns the `LogicLine` object.

**See Also**

* [LineSegment]({{ site.dcvb_python_api }}core/basic-classes/line-segment.html)

### remove_all_logic_lines

Removes all the LogicLines in current object.

```python
def remove_all_logic_lines(self) -> None:
```

### remove_logic_line

Removes a `LogicLine` from current object by specifying an index.

```python
def remove_logic_line(self, index: int) -> int:
```

**Parameters**

`index` The index of the `LogicLine` to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### add_logic_line

Adds a `LogicLine` to current object.

```python
def add_logic_line(self, line: LineSegment, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`line` The `LogicLine` to be added.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### set_logic_line

Sets the `LogicLine` at the specified index.

```python
def set_logic_line(self, index: int, line: LineSegment, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the LogicLine to be set.

`line` The LogicLine to be added.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.
