---
layout: default-layout
title: CDetectedQuadResultItem Class
description: This page shows CDetectedQuadResultItem class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetLocation, GetConfidenceAsDocumentBoundary, GetRotationTransformMatrix, CDetectedQuadResultItem, api reference
---

# CDetectedQuadResultItem Class

The `CDetectedQuadResultItem` class stores a captured result whose type is detected quad.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDetectedQuadResultItem: CCapturedResultItem
```

*Inheritance:* [CCapturedResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html) -> CDetectedQuadResultItem

## Methods

| Method | Description |
|--------|-------------|
| [`GetLocation`](#getlocation) | Gets the location of current object. |
| [`GetConfidenceAsDocumentBoundary`](#getconfidenceasdocumentboundary) | Gets the confidence of current object as a document boundary. |
| [`GetCrossVerificationStatus`](#getcrossverificationstatus) | Gets the status of current object as a verified document boundary. |

### GetLocation

Gets the location of current object.

```cpp
const CQuadrilateral GetLocation() 
```

**Return Value**

The location of current object.

**See Also**

* [CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

### GetConfidenceAsDocumentBoundary

Gets the confidence of current object as a document boundary.

```cpp
int GetConfidenceAsDocumentBoundary() 
```

**Return Value**

The confidence as document boundary of the detected quad result.

### GetCrossVerificationStatus

Gets the status of current object as a verified document boundary.

```cpp
virtual CrossVerificationStatus GetCrossVerificationStatus() const = 0;
```

**Return Value**

The `CrossVerificationStatus` of the detected quad result.

**See Also**

* [CrossVerificationStatus]({{ site.dcvb_cpp_api }}core/enum-cross-verification-status.html)
