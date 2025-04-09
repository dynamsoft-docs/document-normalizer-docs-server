---
layout: default-layout
title: CandidateQuadEdgesUnit Class
description: This page shows CandidateQuadEdgesUnit class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_count, get_candidate_quad_edge, CandidateQuadEdgesUnit, api reference
---

# CandidateQuadEdgesUnit Class

The `CandidateQuadEdgesUnit` class represents an intermediate result unit whose type is candidate quad edges.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class CandidateQuadEdgesUnit(IntermediateResultUnit)
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> CandidateQuadEdgesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`get_count`](#get_count) | Gets the count of `CandidateQuadEdge` objects in current object.|
| [`get_candidate_quad_edge`](#get_candidate_quad_edge) | Gets a `CandidateQuadEdge` object from current object by specifying a index. |
| [`remove_all_candidate_quad_edges`](#remove_all_candidate_quad_edges) | Removes all the candidate quad edges in current object. |
| [`remove_candidate_quad_edge`](#remove_candidate_quad_edge) | Removes a candidate quad edge from current object by specifying an index. |
| [`add_candidate_quad_edge`](#add_candidate_quad_edge) | Adds a candidate quad edge to current object. |
| [`set_candidate_quad_edge`](#set_candidate_quad_edge) | Sets the candidate quad edge at the specified index. |

### get_count

Gets the count of `CandidateQuadEdge` objects in current object.

```python
def get_count(self) -> int:
```

**Return Value**

The count of `CandidateQuadEdge` objects in current object.

### get_candidate_quad_edge

Gets a `CandidateQuadEdge` object from current object by specifying a index.

```python
def get_candidate_quad_edge(self, index: int) -> Tuple[int, Edge]:
```

**Parameters**

`index` The index of the `CandidateQuadEdge` object.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `edge` <*Edge*>: The `CandidateQuadEdge` object got by the specific index.

**See Also**

[EnumErrorCode]({{ site.dcv_python_api }}core/enum-error-code.html)

[Edge]({{ site.dcv_python_api }}core/basic-classes/edge.html)

### remove_all_candidate_quad_edges

Removes all the candidate quad edges in current object.

```python
def remove_all_candidate_quad_edges(self) -> None:
```

### remove_candidate_quad_edge

Removes a candidate quad edge from current object by specifying an index.

```python
def remove_candidate_quad_edge(self, index: int) -> int:
```

**Parameters**

`index` The index of the candidate quad edge to be removed. 

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### add_candidate_quad_edge

Adds a candidate quad edge to current object.

```python
def add_candidate_quad_edge(self, edge: Edge, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`edge` The candidate quad edge to be added.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[Edge]({{ site.dcv_python_api }}core/basic-classes/edge.html)

### set_candidate_quad_edge

Sets the candidate quad edge at the specified index.

```python
def set_candidate_quad_edge(self, index: int, edge: Edge, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the candidate quad edge to be set.

`edge` The candidate quad edge to be added.

`matrix_to_original_image` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[Edge]({{ site.dcv_python_api }}core/basic-classes/edge.html)
