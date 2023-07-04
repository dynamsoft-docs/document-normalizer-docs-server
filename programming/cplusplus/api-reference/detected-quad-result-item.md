---
layout: default-layout
title: CDetectedQuadResultItem Class
description: This page shows CDetectedQuadResultItem class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetLocation, GetConfidenceAsDocumentBoundary, GetRotationTransformMatrix, CDetectedQuadResultItem, api reference
permalink: /programming/cplusplus/api-reference/detected-quad-result-item.html
---

# CDetectedQuadResultItem Class

The CDetectedQuadResultItem class stores a captured result whose type is detected quad.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDetectedQuadResultItem: CCapturedResultItem
```

*Inheritance:* [CCapturedResultItem]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html) -> CDetectedQuadResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetLocation`](#getlocation) | Gets the location of current object. |
| [`GetConfidenceAsDocumentBoundary`](#getconfidenceasdocumentboundary) | Gets the confidence of current object as a document boundary. |

### GetLocation

Gets the location of current object.

```cpp
const CQuadrilateral GetLocation() 
```

**Return Value**

The location of current object.

**See Also**

* [CQuadrilateral]({{ site.dcv_cpp_api }}core/basic-structures/quadrilateral.html)

### GetConfidenceAsDocumentBoundary

Gets the confidence of current object as a document boundary.

```cpp
int GetConfidenceAsDocumentBoundary() 
```

**Return Value**

The confidence as document boundary of the detected quad result.
