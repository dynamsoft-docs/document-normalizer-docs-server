---
layout: default-layout
title: CandidateQuadEdgesUnit Class
description: This page shows CandidateQuadEdgesUnit class definition of Dynamsoft Document Normalizer SDK Java Edition.
keywords: getCount, getCandidateQuadEdge, CandidateQuadEdgesUnit, api reference
---

# CandidateQuadEdgesUnit Class

The `CandidateQuadEdgesUnit` class represents an intermediate result unit whose type is candidate quad edges.

## Definition

*Package:* com.dynamsoft.ddn.intermediate_results

```java
public class CandidateQuadEdgesUnit extends IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> CandidateQuadEdgesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`getCount`](#getcount) | Gets the count of `Edge` objects in current object.|
| [`getCandidateQuadEdge`](#getcandidatequadedge) | Gets an `Edge` object from current object by specifying a index. |
| [`getCandidateQuadEdges`](#getcandidatequadedges) | Gets all `Edge` objects in current object. |
| [`removeAllCandidateQuadEdges`](#removeallcandidatequadedges) | Removes all the candidate quad edges in current object. |
| [`removeCandidateQuadEdge`](#removecandidatequadedge) | Removes a candidate quad edge from current object by specifying an index. |
| [`addCandidateQuadEdge`](#addcandidatequadedge) | Adds a candidate quad edge to current object. |
| [`setCandidateQuadEdge`](#setcandidatequadedge) | Sets the candidate quad edge at the specified index. |

### getCount

Gets the count of `Edge` objects in current object.

```java
public int getCount()
```

**Return Value**

The count of `Edge` objects in current object.

### getCandidateQuadEdge

Gets an `Edge` object from current object by specifying a index.

```java
public Edge getCandidateQuadEdge(int index) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the `Edge` object.

**Return Value**

Returns the `Edge` object got by the specific index.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.md)

**See Also**

[Edge]({{ site.dcvb_java_api }}core/basic-classes/edge.html)

### getCandidateQuadEdges

Gets all `Edge` objects in current object.

```java
public Edge[] getCandidateQuadEdges()
```

**Return Value**

Returns an array of `Edge` objects.

**See Also**

[Edge]({{ site.dcvb_java_api }}core/basic-classes/edge.html)

### removeAllCandidateQuadEdges

Removes all the candidate quad edges in current object.

```java
public void removeAllCandidateQuadEdges()
```

### removeCandidateQuadEdge

Removes a candidate quad edge from current object by specifying an index.

```java
public void removeCandidateQuadEdge(int index) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the candidate quad edge to be removed.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.md)

### addCandidateQuadEdge

Adds a candidate quad edge to current object.

```java
public void addCandidateQuadEdge(Edge edge) throws DocumentNormalizerException
public void addCandidateQuadEdge(Edge edge, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`edge` The candidate quad edge to be added.

`matrixToOriginalImage` The matrix to the original image.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.md)

**See Also**

[Edge]({{ site.dcvb_java_api }}core/basic-classes/edge.html)

### setCandidateQuadEdge

Sets the candidate quad edge at the specified index.

```java
public void setCandidateQuadEdge(int index, Edge edge) throws DocumentNormalizerException
public void setCandidateQuadEdge(int index, Edge edge, double[] matrixToOriginalImage) throws DocumentNormalizerException
```

**Parameters**

`index` The index of the candidate quad edge to be set.

`edge` The candidate quad edge to be added.

`matrixToOriginalImage` The matrix to the original image.

**Exceptions**

[`DocumentNormalizerException`](document-normalizer-exception.md)

**See Also**

[Edge]({{ site.dcvb_java_api }}core/basic-classes/edge.html)
