---
layout: default-layout
title: DetectedQuadResultItem Class - Dynamsoft Document Normalizer Module Java Edition API Reference
description: Definition of DetectedQuadResultItem class in Dynamsoft Document Normalizer Module Java Edition.
keywords: getLocation, getConfidenceAsDocumentBoundary, DetectedQuadResultItem, api reference
---

# DetectedQuadResultItem Class

The `DetectedQuadResultItem` class stores a captured result whose type is detected quad.

## Definition

*Package:* com.dynamsoft.ddn

```java
public class DetectedQuadResultItem extends CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcvb_java_api }}core/basic-classes/captured-result-item.html) -> DetectedQuadResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`getLocation`](#getlocation) | Gets the location of current object. |
| [`getConfidenceAsDocumentBoundary`](#getconfidenceasdocumentboundary) | Gets the confidence of current object as a document boundary. |
| [`getCrossVerificationStatus`](#getcrossverificationstatus) | Gets the status of current object as a verified document boundary. |

### getLocation

Gets the location of current object.

```java
public Quadrilateral getLocation()
```

**Return Value**

The location of current object.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getConfidenceAsDocumentBoundary

Gets the confidence of current object as a document boundary.

```java
public int getConfidenceAsDocumentBoundary()
```

**Return Value**

The confidence as document boundary of the detected quad result.

### getCrossVerificationStatus

Gets the status of current object as a verified document boundary.

```java
public @EnumCrossVerificationStatus int getCrossVerificationStatus()
```

**Return Value**

The status of current object as a verified document boundary.

**See Also**

[EnumCrossVerificationStatus]({{ site.dcvb_java_api }}core/enum-cross-verification-status.html)

