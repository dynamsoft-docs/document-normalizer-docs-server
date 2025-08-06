---
layout: default-layout
title: ProcessedDocumentResult Class
description: This page shows ProcessedDocumentResult class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: ProcessedDocumentResult, api reference
---

# ProcessedDocumentResult Class

The `ProcessedDocumentResult` class is a base class for storing processed document results, including detected quads, deskewed images, and enhanced images. It inherits from `CapturedResultBase`.

## Definition

*Package:* com.dynamsoft.ddn

```java
public class ProcessedDocumentResult extends CapturedResultBase
```

*Inheritance:* [CapturedResultBase]({{ site.dcvb_java_api }}core/basic-classes/captured-result-base.html) -> ProcessedDocumentResult

## Methods

| Method | Description |
|--------|-------------|
| [`getDeskewedImageResultItems`](#getdeskewedimageresultitems)	          | Retrieves the deskewed image result items.     |
| [`getDetectedQuadResultItems`](#getdetectedquadresultitems)	              | Retrieves the detected quad result items.      |
| [`getEnhancedImageResultItems`](#getenhancedimageresultitems)	          | Retrieves the enhanced image result items.     |
| [`getDeskewedImageResultItemsCount`](#getdeskewedimageresultitemscount)	          | Gets the count of deskewed image result items.     |
| [`getDetectedQuadResultItemsCount`](#getdetectedquadresultitemscount)	              | Gets the count of detected quad result items.      |
| [`getEnhancedImageResultItemsCount`](#getenhancedimageresultitemscount)	          | Gets the count of enhanced image result items.     |
| [`getDeskewedImageResultItem`](#getdeskewedimageresultitem)	          | Gets a deskewed image result item by index.     |
| [`getDetectedQuadResultItem`](#getdetectedquadresultitem)	              | Gets a detected quad result item by index.      |
| [`getEnhancedImageResultItem`](#getenhancedimageresultitem)	          | Gets an enhanced image result item by index.     |

### getDeskewedImageResultItems

Retrieves the deskewed image result items.

```java
public DeskewedImageResultItem[] getDeskewedImageResultItems()
```

**Return Value**

Returns an array of `DeskewedImageResultItem` object representing the deskewed image result items.

**See Also**

* [DeskewedImageResultItem]({{ site.ddn_java_api }}deskewed-image-result-item.html)

### getDetectedQuadResultItems

Retrieves the detected quad result items.

```java
public DetectedQuadResultItem[] getDetectedQuadResultItems()
```

**Return Value**

Returns an array of `DetectedQuadResultItem` object representing the detected quad results.

**See Also**

* [DetectedQuadResultItem]({{ site.ddn_java_api }}detected-quad-result-item.html)

### getEnhancedImageResultItems

Retrieves the enhanced image result items.

```java
public EnhancedImageResultItem[] getEnhancedImageResultItems()
```

**Return Value**

Returns an array of `EnhancedImageResultItem` object representing the enhanced image results.

**See Also**

* [EnhancedImageResultItem]({{ site.ddn_java_api }}enhanced-image-result-item.html)

### getDeskewedImageResultItemsCount

Gets the count of deskewed image result items.

```java
public int getDeskewedImageResultItemsCount()
```

**Return Value**

Returns the count of deskewed image result items.

### getDetectedQuadResultItemsCount

Gets the count of detected quad result items.

```java
public int getDetectedQuadResultItemsCount()
```

**Return Value**

Returns the count of detected quad result items.

### getEnhancedImageResultItemsCount

Gets the count of enhanced image result items.

```java
public int getEnhancedImageResultItemsCount()
```

**Return Value**

Returns the count of enhanced image result items.

### getDeskewedImageResultItem

Gets a deskewed image result item by index.

```java
public DeskewedImageResultItem getDeskewedImageResultItem(int index)
```

**Parameters**

`index` The index of the deskewed image result item.

**Return Value**

Returns a `DeskewedImageResultItem` object.

### getDetectedQuadResultItem

Gets a detected quad result item by index.

```java
public DetectedQuadResultItem getDetectedQuadResultItem(int index)
```

**Parameters**

`index` The index of the detected quad result item.

**Return Value**

Returns a `DetectedQuadResultItem` object.

### getEnhancedImageResultItem

Gets an enhanced image result item by index.

```java
public EnhancedImageResultItem getEnhancedImageResultItem(int index)
```

**Parameters**

`index` The index of the enhanced image result item.

**Return Value**

Returns an `EnhancedImageResultItem` object.
