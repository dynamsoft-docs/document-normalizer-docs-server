---
layout: default-layout
title: CDetectedQuadElement Class
description: This page shows CDetectedQuadElement class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetConfidenceAsDocumentBoundary, CDetectedQuadElement, api reference
---

# CDetectedQuadElement Class

The `CDetectedQuadElement` class stores an intermediate result whose type is detected quad.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDetectedQuadElement: CRegionObjectElement
```

*Inheritance:* [CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html) -> CDetectedQuadElement

## Methods

| Method | Description |
|--------|-------------|
| [`GetConfidenceAsDocumentBoundary`](#getconfidenceasdocumentboundary) | Gets the confidence as document boundary of current object. |
| [`SetLocation`](#setlocation) | Sets the location of the detected quad element. |
| **Methods Inherited from [CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html):** | |
| [`GetLocation`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getlocation) | Gets the location of the region object element. |
| [`GetReferencedElement`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getreferencedelement) | Gets a pointer to a referenced region object element. |
| [`GetElementType`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getelementtype) | Gets the type of the region object element. |
| [`GetImageData`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getimagedata) | Gets the imageData of the region object element. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#clone) | Clone the region object element. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#retain) | Increases the reference count of the `CRegionObjectElement` object. |
| [`Release`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#release) | Decreases the reference count of the `CRegionObjectElement` object. |

### GetConfidenceAsDocumentBoundary

Gets the confidence as document boundary of current object.

```cpp
int GetConfidenceAsDocumentBoundary() 
```

**Return Value**

The confidence as document boundary of current object.

### SetLocation

Sets the location of the detected quad element.

```cpp
virtual int SetLocation(const CQuadrilateral& location) = 0;
```

**Parameters**

`location` The location of the detected quad element.

**Return Value**

Returns 0 if success, otherwise an error code.