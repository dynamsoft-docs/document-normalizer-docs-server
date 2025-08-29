---
layout: default-layout
title: DetectedQuadElement Class
description: This page shows DetectedQuadElement class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: getConfidenceAsDocumentBoundary, DetectedQuadElement, api reference
---

# DetectedQuadElement Class

The `DetectedQuadElement` class stores an intermediate result whose type is detected quad.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

```java
public class DetectedQuadElement extends RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html) -> DetectedQuadElement

## Methods

| Method | Description |
|--------|-------------|
| [`DetectedQuadElement`](#detectedquadelement) | Initializes a new instance of the `DetectedQuadElement` class. |
| [`getConfidenceAsDocumentBoundary`](#getconfidenceasdocumentboundary) | Gets the confidence as document boundary of current object. |
| [`setLocation`](#setlocation) | Sets the location of the detected quad element. |

### DetectedQuadElement

Initializes a new instance of the `DetectedQuadElement` class.

```java
public DetectedQuadElement()
```

### getConfidenceAsDocumentBoundary

Gets the confidence as document boundary of current object.

```java
public int getConfidenceAsDocumentBoundary()
```

**Return Value**

The confidence as document boundary of current object.

### setLocation

Sets the location of the detected quad element.

```java
public void setLocation(Quadrilateral location) throws DocumentNormalizerException
```

**Parameters**

`location` The location of the detected quad element.

**Exceptions**

[`DocumentNormalizerException`]({{ site.ddn_java_api }}document-normalizer-exception.html)

**See Also**

* [Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)
