---
layout: default-layout
title: ProcessedDocumentResult Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows ProcessedDocumentResult class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: ProcessedDocumentResult, api reference
---

# ProcessedDocumentResult Class

The `ProcessedDocumentResult` class is a base class for storing processed document results, including detected quads, deskewed images, and enhanced images. It inherits from `CapturedResultBase`.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class ProcessedDocumentResult : CapturedResultBase
```

*Inheritance:* [CapturedResultBase]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-base.html) -> ProcessedDocumentResult

## Methods

| Method | Description |
|--------|-------------|
| [`GetDetectedQuadResultItemsCount`](#getdetectedquadresultitemscount)   |	Gets the count of detected quad result items.                        |
| [`GetDeskewedImageResultItemsCount`](#getdeskewedimageresultitemscount) |	Gets the count of deskewed image result items.                       |
| [`GetEnhancedImageResultItemsCount`](#getenhancedimageresultitemscount) |	Gets the count of enhanced image result items.                       |
| [`GetDeskewedImageResultItem`](#getdeskewedimageresultitem)	          | Retrieves the deskewed image result item at the specified index.     |
| [`GetDetectedQuadResultItem`](#getdetectedquadresultitem)	              | Retrieves the detected quad result item at the specified index.      |
| [`GetEnhancedImageResultItem`](#getenhancedimageresultitem)	          | Retrieves the enhanced image result item at the specified index.     |
| [`GetDeskewedImageResultItems`](#getdeskewedimageresultitems)	          | Retrieves all the deskewed image result items.     |
| [`GetDetectedQuadResultItems`](#getdetectedquadresultitems)	              | Retrieves all the detected quad result items.      |
| [`GetEnhancedImageResultItems`](#getenhancedimageresultitems)	          | Retrieves all the enhanced image result items.     |

### GetDetectedQuadResultItemsCount

Gets the count of detected quad result items.

```csharp
int GetDetectedQuadResultItemsCount()
```

**Return Value**

Returns the number of detected quad result items.

### GetDeskewedImageResultItemsCount

Gets the count of deskewed image result items.

```csharp
int GetDeskewedImageResultItemsCount()
```

**Return Value**

Returns the number of deskewed image result items.

### GetEnhancedImageResultItemsCount

Gets the count of enhanced image result items.

```csharp
int GetEnhancedImageResultItemsCount()
```

**Return Value**

Returns the number of enhanced image result items.

### GetDeskewedImageResultItem

Retrieves the deskewed image result item at the specified index.

```csharp
DeskewedImageResultItem GetDeskewedImageResultItem(int index)
```

**Parameters**

`[in] index` The index of the deskewed image result item to retrieve.

**Return Value**

Returns a `DeskewedImageResultItem` object representing the deskewed image result at the specified index.

**See Also**

* [DeskewedImageResultItem]({{ site.ddn_dotnet_api }}deskewed-image-result-item.html)

### GetDetectedQuadResultItem

Retrieves the detected quad result item at the specified index.

```csharp
DetectedQuadResultItem GetDetectedQuadResultItem(int index)
```

**Parameters**

`[in] index` The index of the detected quad result item to retrieve.

**Return Value**

Returns a `DetectedQuadResultItem` object representing the detected quad result at the specified index.

**See Also**

* [DetectedQuadResultItem]({{ site.ddn_dotnet_api }}detected-quad-result-item.html)

### GetEnhancedImageResultItem

Retrieves the enhanced image result item at the specified index.

```csharp
EnhancedImageResultItem GetEnhancedImageResultItem(int index)
```

**Parameters**

`[in] index` The index of the enhanced image result item to retrieve.

**Return Value**

Returns a `EnhancedImageResultItem` object representing the enhanced image result at the specified index.

**See Also**

* [EnhancedImageResultItem]({{ site.ddn_dotnet_api }}enhanced-image-result-item.html)

### GetDeskewedImageResultItems

Retrieves all the deskewed image result items.

```csharp
DeskewedImageResultItem[] GetDeskewedImageResultItems()
```

**Return Value**

Returns a `DeskewedImageResultItem` object array representing all the deskewed image results.

**See Also**

* [DeskewedImageResultItem]({{ site.ddn_dotnet_api }}deskewed-image-result-item.html)

### GetDetectedQuadResultItems

Retrieves all the detected quad result items.

```csharp
DetectedQuadResultItem[] GetDetectedQuadResultItems()
```

**Return Value**

Returns a `DetectedQuadResultItem` object array representing all the detected quad results.

**See Also**

* [DetectedQuadResultItem]({{ site.ddn_dotnet_api }}detected-quad-result-item.html)

### GetEnhancedImageResultItems

Retrieves all the enhanced image result items.

```csharp
EnhancedImageResultItem[] GetEnhancedImageResultItems()
```

**Return Value**

Returns an `EnhancedImageResultItem` object array representing all the enhanced image results.

**See Also**

* [EnhancedImageResultItem]({{ site.ddn_dotnet_api }}enhanced-image-result-item.html)

