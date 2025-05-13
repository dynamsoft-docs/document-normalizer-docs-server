---
layout: default-layout
title: DetectedQuadsResult Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: Definition of DetectedQuadsResult class in Dynamsoft Document Normalizer Module .NET Edition.
keywords: GetItemsCount, GetErrorCode, GetErrorString, GetItem, GetOriginalImageHashId, GetOriginalImageTag, DetectedQuadsResult, api reference
---

# DetectedQuadsResult Class

The DetectedQuadsResult class stores a captured result whose type is detected quads.

## Definition

*Namespace:* Dynamsoft.DDN


```csharp
public class DetectedQuadsResult
```

## Methods

| Method | Description |
|--------|-------------|
| [`GetErrorCode`](#geterrorcode) | Gets the error code of the detection operation. |
| [`GetErrorString`](#geterrorstring) | Gets the error message of the detection operation. |
| [`GetItems`](#getitems) | Gets the detected quadrilateral item at a specified index. |
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image. |

### GetErrorCode

Gets the error code of the detection operation.

```csharp
int GetErrorCode()
```

**Return Value**

Returns the error code.

**See Also**

* [EnumErrorCode]({{ site.dcvb_enumerations }}core/error-code.html)

### GetErrorString

Gets the error message of the detection operation.

```csharp
string GetErrorString()
```

**Return Value**

Returns a string that represents the error message.

### GetItems

Gets the detected quadrilateral item at a specified index.

```csharp
DetectedQuadResultItem GetItems()
```

**Parameters**

`[in] index` The index of the detected quadrilateral to retrieve.

**Return Value**

Returns a `DetectedQuadResultItem` object that represents the detected quadrilateral at the specified index.

**See Also**

* [DetectedQuadResultItem](detected-quad-result-item.md)

### GetRotationTransformMatrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```csharp
double[] GetRotationTransformMatrix()
```

**Return Value**

Returns a double array of length 9 which represents a 3x3 rotation matrix.

### GetOriginalImageHashId

Gets the hash ID of the original image.

```csharp
string GetOriginalImageHashId()
```

**Return Value**

Returns a string that represents the hash ID of the original image.

### GetOriginalImageTag

Gets the tag of the original image.

```csharp
ImageTag GetOriginalImageTag()
```

**Return Value**

Returns an `ImageTag` object that represents the tag of the original image.

**See Also**

* [ImageTag]({{ site.dcvb_dotnet_api }}core/basic-classes/image-tag.html)

