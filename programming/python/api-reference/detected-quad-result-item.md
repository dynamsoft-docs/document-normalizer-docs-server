---
layout: default-layout
title: DetectedQuadResultItem Class - Dynamsoft Document Normalizer Module Python Edition API Reference
description: Definition of DetectedQuadResultItem class in Dynamsoft Document Normalizer Module Python Edition.
keywords: get_location, get_confidence_as_document_boundary, DetectedQuadResultItem, api reference
---

# DetectedQuadResultItem Class

The `DetectedQuadResultItem` class stores a captured result whose type is detected quad.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class DetectedQuadResultItem(dynamsoft_core.CapturedResultItem)
```

*Inheritance:* [CapturedResultItem]({{ site.dcvb_python_api }}core/basic-classes/captured-result-item.html) -> DetectedQuadResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`get_location`](#get_location) | Gets the location of current object. |
| [`get_confidence_as_document_boundary`](#get_confidence_as_document_boundary) | Gets the confidence of current object as a document boundary. |

### get_location

Gets the location of current object.

```python
def get_location(self) -> Quadrilateral:
```

**Return Value**

The location of current object.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### get_confidence_as_document_boundary

Gets the confidence of current object as a document boundary.

```python
def get_confidence_as_document_boundary(self) -> int:
```

**Return Value**

The confidence as document boundary of the detected quad result.
