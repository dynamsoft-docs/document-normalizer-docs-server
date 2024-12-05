---
layout: default-layout
title: DetectedQuadElement Class
description: This page shows DetectedQuadElement class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: get_confidence_as_document_boundary, DetectedQuadElement, api reference
---

# DetectedQuadElement Class

The `DetectedQuadElement` class stores an intermediate result whose type is detected quad.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class DetectedQuadElement(RegionObjectElement)
```

*Inheritance:* [RegionObjectElement]({{ site.dcv_python_api }}core/intermediate-results/region-object-element.html) -> DetectedQuadElement

## Methods

| Method | Description |
|--------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `DetectedQuadElement` class. |
| [`get_confidence_as_document_boundary`](#get_confidence_as_document_boundary) | Gets the confidence as document boundary of current object. |

### \_\_init\_\_

Initializes a new instance of the `DetectedQuadElement` class.

```python
def __init__(self, *args, **kwargs):
```

### get_confidence_as_document_boundary

Gets the confidence as document boundary of current object.

```python
def get_confidence_as_document_boundary(self) -> int:
```

**Return Value**

The confidence as document boundary of current object.
