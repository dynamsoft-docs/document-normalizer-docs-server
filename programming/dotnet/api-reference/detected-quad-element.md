---
layout: default-layout
title: DetectedQuadElement Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: API reference for the DetectedQuadElement class in Dynamsoft Document Normalizer .NET Edition, which represents an intermediate result element containing a detected quadrilateral boundary of a document.
keywords: GetConfidenceAsDocumentBoundary, DetectedQuadElement, api reference
---

# DetectedQuadElement Class

The `DetectedQuadElement` class stores an intermediate result whose type is detected quad.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class DetectedQuadElement : RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html) -> DetectedQuadElement

## Methods

| Method | Description |
|--------|-------------|
| [`GetConfidenceAsDocumentBoundary`](#getconfidenceasdocumentboundary) | Gets the confidence as document boundary of current object. |
| [`SetLocation`](#setlocation) | Sets the location of the detected quad element. |

### GetConfidenceAsDocumentBoundary

Gets the confidence as document boundary of current object.

```csharp
int GetConfidenceAsDocumentBoundary() 
```

**Return Value**

The confidence as document boundary of current object.

### SetLocation

Sets the location of the detected quad element.

```csharp
int SetLocation(Quadrilateral location)
```

**Parameters**

`location` The location of the detected quad element.

**Return Value**

Returns 0 if success, otherwise an error code.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)
