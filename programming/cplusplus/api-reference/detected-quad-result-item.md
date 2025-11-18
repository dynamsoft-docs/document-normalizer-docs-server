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
| Methods Inherited from [CCapturedResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html): | |
| [`GetType`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#gettype) | Gets the type of the captured result item. |
| [`GetReferenceItem`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#getreferenceitem) | Gets a pointer to the referenced item in the captured result. |
| [`GetTargetROIDefName`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#gettargetroidefname) | Gets the name of the target ROI definition. |
| [`GetTaskName`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#gettaskname) | Gets the name of the task. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#retain) | Increases the reference count of the `CCapturedResultItem` object. |
| [`Release`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#release) | Decreases the reference count of the `CCapturedResultItem` object. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#clone) | Clone the captured result item. |

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
