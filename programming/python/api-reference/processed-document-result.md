---
layout: default-layout
title: ProcessedDocumentResult Class
description: This page shows ProcessedDocumentResult class definition of Dynamsoft Document Normalizer SDK Python Edition.
keywords: ProcessedDocumentResult, api reference
---

# ProcessedDocumentResult Class

The `ProcessedDocumentResult` class is a base class for storing processed document results, including detected quads, deskewed images, and enhanced images. It inherits from `CapturedResultBase`.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class ProcessedDocumentResult(CapturedResultBase):
```

*Inheritance:* [CapturedResultBase]({{ site.dcv_python_api }}core/basic-classes/captured-result-base.html) -> ProcessedDocumentResult

## Methods

| Method | Description |
|--------|-------------|
| [`get_deskewed_image_result_items`](#get_deskewed_image_result_items)	          | Retrieves the deskewed image result items.     |
| [`get_detected_quad_result_items`](#get_detected_quad_result_items)	              | Retrieves the detected quad result items.      |
| [`get_enhanced_image_result_items`](#get_enhanced_image_result_items)	          | Retrieves the enhanced image result items.     |

### get_deskewed_image_result_items

Retrieves the deskewed image result items.

```python
def get_deskewed_image_result_items(self) -> List[DeskewedImageResultItem]:
```

**Return Value**

Returns a list of `DeskewedImageResultItem` object representing the deskewed image result items.

**See Also**

* [DeskewedImageResultItem]({{ site.ddn_python_api }}deskewed-image-result-item.html)

### get_detected_quad_result_items

Retrieves the detected quad result items.

```python
def get_detected_quad_result_items(self) -> List[DetectedQuadResultItem]:
```

**Return Value**

Returns a list of `DetectedQuadResultItem` object representing the detected quad results.

**See Also**

* [DetectedQuadResultItem]({{ site.ddn_python_api }}detected-quad-result-item.html)

### get_enhanced_image_result_items

Retrieves the enhanced image result items.

```python
def get_enhanced_image_result_items(self) -> List[EnhancedImageResultItem]:
```

**Return Value**

Returns a list of `EnhancedImageResultItem` object representing the enhanced image results.

**See Also**

* [EnhancedImageResultItem]({{ site.ddn_python_api }}enhanced-image-result-item.html)
