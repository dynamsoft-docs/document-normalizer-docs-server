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

*Inheritance:* [CIntermediateResultUnit]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CCandidateQuadEdgesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of CandidateQuadEdge objects in current object.|
| [`GetCandidateQuadEdge`](#getcandidatequadedge) | Gets a CandidateQuadEdge object from current object by specifying a index. |
| [`RemoveAllCandidateQuadEdges`](#removeallcandidatequadedges) | Removes all the candidate quad edges in current object. |
| [`RemoveCandidateQuadEdge`](#removecandidatequadedge) | Removes a candidate quad edge from current object by specifying an index. |
| [`AddCandidateQuadEdge`](#addcandidatequadedge) | Adds a candidate quad edge to current object. |
| [`SetCandidateQuadEdge`](#setcandidatequadedge) | Sets the candidate quad edge at the specified index. |

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

* [CEdge]({{ site.dcv_cpp_api }}core/basic-structures/edge.html)
* [ErrorCode]({{ site.enumerations }}core/error-code.html?src=cpp&&lang=cpp)

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