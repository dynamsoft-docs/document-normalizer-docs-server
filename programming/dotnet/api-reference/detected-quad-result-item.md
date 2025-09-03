---
layout: default-layout
title: DetectedQuadResultItem Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: Definition of DetectedQuadResultItem class in Dynamsoft Document Normalizer Module .NET Edition.
keywords: GetLocation, GetConfidenceAsDocumentBoundary, GetRotationTransformMatrix, DetectedQuadResultItem, api reference
---

# DetectedQuadResultItem Class

The `DetectedQuadResultItem` class stores a captured result whose type is detected quad.

## Definition

*Namespace:* Dynamsoft.DDN

*Assembly:* Dynamsoft.DocumentNormalizer.dll

```csharp
public class DetectedQuadResultItem: CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-item.html) -> DetectedQuadResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetLocation`](#getlocation) | Gets the location of current object. |
| [`GetConfidenceAsDocumentBoundary`](#getconfidenceasdocumentboundary) | Gets the confidence of current object as a document boundary. |

### GetLocation

Gets the location of current object.

```csharp
Quadrilateral GetLocation() 
```

**Return Value**

The location of current object.

**See Also**

* [Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### GetConfidenceAsDocumentBoundary

Gets the confidence of current object as a document boundary.

```csharp
int GetConfidenceAsDocumentBoundary() 
```

**Return Value**

The confidence as document boundary of the detected quad result.
