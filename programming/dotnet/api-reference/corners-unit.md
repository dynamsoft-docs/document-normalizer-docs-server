---
layout: default-layout
title: CornersUnit Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: This page shows CornersUnit class definition of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: GetCount, GetCorner, CornersUnit, api reference
---

# CornersUnit Class

The `CornersUnit` class represents an intermediate result unit whose type is corners.

## Definition

*Namespace:* Dynamsoft.DDN.intermediate_results


```csharp
class CornersUnit : IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> CornersUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the count of `Corner` objects in current object.|
| [`GetCorner`](#getcorner) | Gets a `Corner` object from current object by specifying a index. |
| [`GetCorners`](#getcorners) | Gets all `Corner` objects from current object. |
| [`RemoveAllCorners`](#removeallcorners) | Removes all the `Corner` objects in current object. |
| [`RemoveCorner`](#removecorner) | Removes a `Corner` from current object by specifying an index. |
| [`AddCorner`](#addcorner) | Adds a `Corner` to current object. |
| [`SetCorner`](#setcorner) | Sets the `Corner` at the specified index. |

### GetCount

Gets the count of `Corner` objects in current object.

```csharp
int GetCount() 
```

**Return Value**

The count of `Corner` objects in current object.

### GetCorner

Gets a `Corner` object from current object by specifying a index.

```csharp
int GetCorner(int index, out Corner corner)
```

**Parameters**

`[in] index` The index of the `Corner` object.

`[in, out] corner` the `Corner` object got by the specific index.

**Return Value**

Returns the error code.

**See Also**

* [Corner]({{ site.dcvb_dotnet_api }}core/basic-classes/corner.html)
* [ErrorCode]({{ site.dcvb_dotnet_api }}core/enum-error-code.html)

### GetCorners

Gets all `Corner` objects from current object.

```csharp
int GetCorners(out Corner[] corners)
```

**Parameters**

`[in, out] corners` All the `Corner` objects got by the specific index.

**Return Value**

Returns the error code.

**See Also**

* [Corner]({{ site.dcvb_dotnet_api }}core/basic-classes/corner.html)
* [ErrorCode]({{ site.dcvb_dotnet_api }}core/enum-error-code.html)

### RemoveAllCorners

Removes all the `Corner`s in current object.

```csharp
void RemoveAllCorners()
```

### RemoveCorner

Removes a `Corner` from current object by specifying an index.

```csharp
int RemoveCorner(int index)
```

**Parameters**

`[in] index` The index of the `Corner` to be removed.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

### AddCorner

Adds a `Corner` to current object.

```csharp
int AddCorner(Corner corner, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] corner` the `Corner` to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [Corner]({{ site.dcvb_dotnet_api }}core/basic-classes/corner.html)

### SetCorner

Sets the `Corner` at the specified index.

```csharp
int SetCorner(int index, Corner corner, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] index` The index of the `Corner` to be set.

`[in] corner` the `Corner` to be added.

`[in] matrixToOriginalImage` The matrix to the original image.

**Return Value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

* [Corner]({{ site.dcvb_dotnet_api }}core/basic-classes/corner.html)
