---
layout: default-layout
title: NormalizedImagesResult Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: Definition of NormalizedImagesResult class in Dynamsoft Document Normalizer Module .NET Edition.
keywords: GetItemsCount, GetErrorCode, GetErrorString, GetItem, GetOriginalImageHashId, GetOriginalImageTag, NormalizedImagesResult, api reference
---

# NormalizedImagesResult

The NormalizedImagesResult class stores a collection of captured result items whose type are normalized images.

## Definition

*Namespace:* Dynamsoft.DDN

*Assembly:* Dynamsoft.DocumentNormalizer.dll

```csharp
public class NormalizedImagesResult : CRegionObjectElement
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetErrorCode`](#geterrorcode) | Gets the error code of the operation. |
| [`GetErrorString`](#geterrorstring) | Gets the error message of the operation. |
| [`GetItems`](#getitems) | Gets a specific normalized image from the result. |
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image, from which you get the normalized image. |
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image, from which you get the normalized image. |

### GetErrorCode

Gets the error code of the operation.

```csharp
int GetErrorCode()
```

**Return Value**

Returns the error code of the operation. A non-zero value indicates an error occurred.

**See Also**

* [EnumErrorCode]({{ site.dcv_enumerations }}core/error-code.html?lang=dotnet)

### GetErrorString

Gets the error message of the operation.

```csharp
string GetErrorString()
```

**Return Value**

Returns the error message of the operation.

### GetItems

Gets a specific normalized image from the result.

```csharp
NormalizedImageResultItem GetItems
```

**Parameters**

`[in] index` The index of the normalized image to get.

**Return Value**

Returns a normalized image at the specified index. If the index is out of range, returns nullptr.

**See Also**

* [NormalizedImageResultItem](normalized-image-result-item.md)

### GetRotationTransformMatrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```csharp
double[] GetRotationTransformMatrix()
```

**Return Value**

Returns a double array of length 9 which represents a 3x3 rotation matrix.

### GetOriginalImageHashId

Gets the hash ID of the original image that was normalized.

```csharp
string GetOriginalImageHashId()
```

**Return Value**

Returns the hash ID of the original image that was normalized.

### GetOriginalImageTag

Gets the tag of the original image that was normalized.

```csharp
ImageTag GetOriginalImageTag()
```

**Return Value**

Returns a tag of the original image that was normalized.

**See Also**

* [ImageTag]({{ site.dcv_dotnet_api }}core/basic-classes/image-tag.html)
