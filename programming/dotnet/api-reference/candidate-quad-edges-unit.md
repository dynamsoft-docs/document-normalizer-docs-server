---
layout: default-layout
title: CandidateQuadEdgesUnit Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows CandidateQuadEdgesUnit class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetCount, GetCandidateQuadEdge, CandidateQuadEdgesUnit, api reference
---

# CandidateQuadEdgesUnit Class

The `CandidateQuadEdgesUnit` class represents an intermediate result unit whose type is candidate quad edges.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class CandidateQuadEdgesUnit : IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> CandidateQuadEdgesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of `CandidateQuadEdge` objects in current object.|
| [`GetCandidateQuadEdge`](#getcandidatequadedge) | Gets a `CandidateQuadEdge` object from current object by specifying a index. |
| [`GetCandidateQuadEdges`](#getcandidatequadedges) | Gets all `CandidateQuadEdge` objects from current object. |
| [`RemoveAllCandidateQuadEdges`](#removeallcandidatequadedges) | Removes all the candidate quad edges in current object. |
| [`RemoveCandidateQuadEdge`](#removecandidatequadedge) | Removes a candidate quad edge from current object by specifying an index. |
| [`AddCandidateQuadEdge`](#addcandidatequadedge) | Adds a candidate quad edge to current object. |
| [`SetCandidateQuadEdge`](#setcandidatequadedge) | Sets the candidate quad edge at the specified index. |

### GetCount

Gets the count of `CandidateQuadEdge` objects in current object.

```csharp
int GetCount() 
```

**Return Value**

The count of `CandidateQuadEdge` objects in current object.

### GetCandidateQuadEdge

Gets a `CandidateQuadEdge` object from current object by specifying a index.

```csharp
int GetCandidateQuadEdge(int index, out Edge edge)
```

**Parameters**

`[in] index` The index of the `CandidateQuadEdge` object.

`[in, out] edge` The `CandidateQuadEdge` object got by the specific index.

**Return Value**

Returns the error code.

**See Also**

* [Edge]({{ site.dcvb_dotnet_api }}core/basic-classes/edge.html)
* [ErrorCode]({{ site.dcvb_enumerations }}core/error-code.html)

### GetCandidateQuadEdges

Gets all `CandidateQuadEdge` objects from current object.

```csharp
int GetCandidateQuadEdges(out Edge[] edges)
```

**Parameters**

`[in, out] edges` All the `CandidateQuadEdge` objects got from current object.

**Return Value**

Returns the error code.

**See Also**

* [Edge]({{ site.dcvb_dotnet_api }}core/basic-classes/edge.html)
* [ErrorCode]({{ site.dcvb_enumerations }}core/error-code.html)

### RemoveAllCandidateQuadEdges

Removes all the candidate quad edges in current object.

```csharp
void RemoveAllCandidateQuadEdges()
```

### RemoveCandidateQuadEdge

Removes a candidate quad edge from current object by specifying an index.

```csharp
int RemoveCandidateQuadEdge(int index)
```

**Parameters**

`[in] index` The index of the candidate quad edge to be removed. 

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddCandidateQuadEdge

Adds a candidate quad edge to current object.

```csharp
int AddCandidateQuadEdge(Edge edge, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] edge` The candidate quad edge to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [Edge]({{ site.dcvb_dotnet_api }}core/basic-classes/edge.html)

### SetCandidateQuadEdge

Sets the candidate quad edge at the specified index.

```csharp
int SetCandidateQuadEdge(int index, Edge edge, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] index` The index of the candidate quad edge to be set.

`[in] edge` The candidate quad edge to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [Edge]({{ site.dcvb_dotnet_api }}core/basic-classes/edge.html)
