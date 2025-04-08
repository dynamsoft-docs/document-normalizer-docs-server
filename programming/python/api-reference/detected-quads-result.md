---
layout: default-layout
title: DetectedQuadsResult Class - Dynamsoft Document Normalizer Module Python Edition API Reference
description: Definition of DetectedQuadsResult class in Dynamsoft Document Normalizer Module Python Edition.
keywords: get_items, get_error_code, get_error_string, get_original_image_hash_id, get_original_image_tag, DetectedQuadsResult, api reference
---

# DetectedQuadsResult Class

The `DetectedQuadsResult` class stores a captured result whose type is detected quads.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class DetectedQuadsResult
```

## Methods

| Method | Description |
|--------|-------------|
| [`get_error_code`](#get_error_code) | Gets the error code of the detection operation. |
| [`get_error_string`](#get_error_string) | Gets the error message of the detection operation. |
| [`get_items`](#get_items) | Gets the detected quadrilateral item at a specified index. |
| [`get_rotation_transform_matrix`](#get_rotation_transform_matrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`get_original_image_hash_id`](#get_original_image_hash_id) | Gets the hash ID of the original image. |
| [`get_original_image_tag`](#get_original_image_tag) | Gets the tag of the original image. |

### get_error_code

Gets the error code of the detection operation.

```python
def get_error_code(self) -> int:
```

**Return Value**

Returns the error code.

**See Also**

[EnumErrorCode]({{ site.dcv_python_api }}core/enum-error-code.html)

### get_error_string

Gets the error message of the detection operation.

```python
def get_error_string(self) -> str:
```

**Return Value**

Returns a string that represents the error message.

### get_items

Gets all the detected quadrilateral items.

```python
def get_items(self) -> List[DetectedQuadResultItem]:
```

**Return Value**

Returns a `DetectedQuadResultItem` list.

**See Also**

[DetectedQuadResultItem]({{ site.ddn_python_api }}detected-quad-result-item.html)

### get_rotation_transform_matrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```python
def get_rotation_transform_matrix(self) -> List[float]:
```

**Return Value**

Returns a float list of length 9 which represents a 3x3 rotation matrix.

### get_original_image_hash_id

Gets the hash ID of the original image.

```python
def get_original_image_hash_id(self) -> str:
```

**Return Value**

Returns a string that represents the hash ID of the original image.

### get_original_image_tag

Gets the tag of the original image.

```python
def get_original_image_tag(self) -> ImageTag:
```

**Return Value**

Returns an `ImageTag` object that represents the tag of the original image.

**See Also**

[ImageTag]({{ site.dcv_python_api }}core/basic-classes/image-tag.html)

