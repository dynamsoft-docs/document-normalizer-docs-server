---
layout: default-layout
title: NormalizedImagesResult Class - Dynamsoft Document Normalizer Module Python Edition API Reference
description: Definition of NormalizedImagesResult class in Dynamsoft Document Normalizer Module Python Edition.
keywords: get_items, get_error_code, get_error_string, get_original_image_hash_id, get_original_image_tag, NormalizedImagesResult, api reference
---

# NormalizedImagesResult

The NormalizedImagesResult class stores a collection of captured result items whose type are normalized images.

## Definition

*Module:* dynamsoft_document_normalizer

```python
class NormalizedImagesResult
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_error_code`](#get_error_code) | Gets the error code of the operation. |
| [`get_error_string`](#get_error_string) | Gets the error message of the operation. |
| [`get_items`](#get_items) | Gets a specific normalized image from the result. |
| [`get_rotation_transform_matrix`](#get_rotation_transform_matrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`get_original_image_hash_id`](#get_original_image_hash_id) | Gets the hash ID of the original image, from which you get the normalized image. |
| [`get_original_image_tag`](#get_original_image_tag) | Gets the tag of the original image, from which you get the normalized image. |

### get_error_code

Gets the error code of the operation.

```python
def get_error_code(self) -> int:
```

**Return Value**

Returns the error code of the operation. A non-zero value indicates an error occurred.

**See Also**

[EnumErrorCode]({{ site.dcv_python_api }}core/enum-error-code.html)

### get_error_string

Gets the error message of the operation.

```python
def get_error_string(self) -> str:
```

**Return Value**

Returns the error message of the operation.

### get_items

Gets all the normalized images.

```python
def get_items(self) -> List[NormalizedImageResultItem]:
```

**Return Value**

Returns a `NormalizedImageResultItem` list.

**See Also**

[NormalizedImageResultItem]({{ site.ddn_python_api }}normalized-image-result-item.html)

### get_rotation_transform_matrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```python
def get_rotation_transform_matrix(self) -> List[float]:
```

**Return Value**

Returns a float list of length 9 which represents a 3x3 rotation matrix.

### get_original_image_hash_id

Gets the hash ID of the original image that was normalized.

```python
def get_original_image_hash_id(self) -> str:
```

**Return Value**

Returns the hash ID of the original image that was normalized.

### get_original_image_tag

Gets the tag of the original image that was normalized.

```python
def get_original_image_tag(self) -> ImageTag:
```

**Return Value**

Returns a tag of the original image that was normalized.

**See Also**

[ImageTag]({{ site.dcv_python_api }}core/basic-classes/image-tag.html)
