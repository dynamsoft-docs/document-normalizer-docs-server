---
layout: default-layout
title: CCandidateQuadEdgesUnit Class
description: This page shows CCandidateQuadEdgesUnit class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: GetCount, GetCandidateQuadEdge, CCandidateQuadEdgesUnit, api reference
permalink: /programming/cplusplus/api-reference/candidate-quad-edges-unit.html
---

# CCandidateQuadEdgesUnit Class

The CCandidateQuadEdgesUnit class represents an intermediate result unit whose type is candidate quad edges.

## Definition

*Namespace:* dynamsoft::ddn::intermediate_results

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CCandidateQuadEdgesUnit: CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CCandidateQuadEdgesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of CandidateQuadEdge objects in current object.|
| [`GetCandidateQuadEdge`](#getcandidatequadedge) | Gets a CandidateQuadEdge object from current object by specifying a index. |
| [`RemoveAllCandidateQuadEdges`](#removeallcandidatequadedges) | Removes all the candidate quad edges in current object. |
| [`RemoveCandidateQuadEdge`](#removecandidatequadedge) | Removes a candidate quad edge from current object by specifying an index. |
| [`AddCandidateQuadEdge`](#addcandidatequadedge) | Adds a candidate quad edge to current object. |
| [`SetCandidateQuadEdge`](#setcandidatequadedge) | Sets the candidate quad edge at the specified index. |
| Methods Inherited from [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html): | |
| [`GetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit.|
| [`GetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the image tag of the original image. |
| [`GetType`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`SetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#sethashid) | Sets the hash ID of the unit. |
| [`SetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagehashid) | Sets the hash ID of the original image. |
| [`SetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagetag) | Sets the image tag of the original image. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#retain) | Increases the reference count of the unit. |
| [`Release`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#release) | Decreases the reference count of the unit. |
| [`GetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via TransformMatrixType. |
| [`SetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#settransformmatrix) | Sets the transformation matrix via TransformMatrixType. |

### GetCount

Gets the count of CandidateQuadEdge objects in current object.

```cpp
int GetCount() 
```

**Return Value**

The count of CandidateQuadEdge objects in current object.

### GetCandidateQuadEdge

Gets a CandidateQuadEdge object from current object by specifying a index.

```cpp
int GetCandidateQuadEdge(int index, CEdge* edge)
```

**Parameters**

`[in] index` The index of the CandidateQuadEdge object.

`[in, out] edge` The CandidateQuadEdge object got by the specific index.

**Return Value**

Returns the error code.

**See Also**

* [CEdge]({{ site.dcvb_cpp_api }}core/basic-structures/edge.html)
* [ErrorCode]({{ site.dcvb_cpp_api }}core/enum-error-code.html)

### RemoveAllCandidateQuadEdges

Removes all the candidate quad edges in current object.

```cpp
virtual void RemoveAllCandidateQuadEdges() = 0
```

### RemoveCandidateQuadEdge

Removes a candidate quad edge from current object by specifying an index.

```cpp
virtual int RemoveCandidateQuadEdge(int index) = 0
```

**Parameters**

`[in] index` The index of the candidate quad edge to be removed. 

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddCandidateQuadEdge

Adds a candidate quad edge to current object.

```cpp
virtual int AddCandidateQuadEdge(const CEdge& edge, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0
```

**Parameters**

`[in] edge` The candidate quad edge to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### SetCandidateQuadEdge

Sets the candidate quad edge at the specified index.

```cpp
virtual int SetCandidateQuadEdge(int index, const CEdge& edge, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] index` The index of the candidate quad edge to be set.

`[in] edge` The candidate quad edge to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.