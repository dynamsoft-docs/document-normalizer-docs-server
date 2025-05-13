---
layout: default-layout
title: DetectedQuadsUnit Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows DetectedQuadsUnit class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetCount, GetDetectedQuad, DetectedQuadsUnit, api reference
---

# DetectedQuadsUnit Class

The `DetectedQuadsUnit` class represents an intermediate result unit whose type is detected quads.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class DetectedQuadsUnit : IntermediateResultUnit, IEnumerable<DetectedQuadElement>
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> DetectedQuadsUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of `DetectedQuadElement` objects in current object.|
| [`GetDetectedQuad`](#getdetectedquad) | Gets a `DetectedQuadElement` object from current object by specifying a index. |
| [`GetDetectedQuads`](#getdetectedquads) | Gets all `DetectedQuadElement` objects from current object. |
| [`RemoveAllDetectedQuads`](#removealldetectedquads) | Removes all the detected quads in current object. |
| [`RemoveDetectedQuad`](#removedetectedquad) | Removes a detected quad from current object by specifying an index. |
| [`AddDetectedQuad`](#adddetectedquad) | Adds a detected quad to current object. |
| [`SetDetectedQuad`](#setdetectedquad) | Sets the detected quad at the specified index. |

### GetCount

Gets the count of `DetectedQuadElement` objects in current object.

```csharp
int GetCount() 
```

**Return Value**

The count of `DetectedQuadElement` objects in current object.

### GetDetectedQuad

Gets a `DetectedQuadElement` object from current object by specifying a index.

```csharp
DetectedQuadElement GetDetectedQuad(int index)
```

**Parameters**

`[in] index` The index of the `DetectedQuadElement` object.

**Return Value**

Returns the `DetectedQuadElement` object got by the specific index.

**See Also**

* [DetectedQuadElement]({{ site.ddn_dotnet_api }}detected-quad-element.html)

### GetDetectedQuads

Gets all `DetectedQuadElement` objects from current object.

```csharp
DetectedQuadElement[] GetDetectedQuads()
```

**Return Value**

Returns all the `DetectedQuadElement` objects got from current object.

**See Also**

* [DetectedQuadElement]({{ site.ddn_dotnet_api }}detected-quad-element.html)

### RemoveAllDetectedQuads

Removes all the DetectedQuads in current object.

```csharp
void RemoveAllDetectedQuads()
```

### RemoveDetectedQuad

Removes a detected quad from current object by specifying an index.

```csharp
int RemoveDetectedQuad(int index)
```

**Parameters**

`[in] index` The index of the detected quad to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddDetectedQuad

Adds a `DetectedQuadElement` to current object.

```csharp
int AddDetectedQuad(DetectedQuadElement element, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] element` The detected quad to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [DetectedQuadElement]({{ site.ddn_dotnet_api }}detected-quad-element.html)

### SetDetectedQuad

Sets the `DetectedQuadElement` at the specified index.

```csharp
int SetDetectedQuad(int index, DetectedQuadElement element, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] index` The index of the detected quad to be set.

`[in] element` The detected quad to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [DetectedQuadElement]({{ site.ddn_dotnet_api }}detected-quad-element.html)
