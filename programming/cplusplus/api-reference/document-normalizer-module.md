---
layout: default-layout
title: class CDocumentNormalizerModule - Dynamsoft Document Normalizer Classes
description: This page shows the C++ edition of the class CDocumentNormalizerModule in Document Normalizer Module.
keywords: document normalizer module, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: C++ CDocumentNormalizerModule Class
permalink: /programming/cplusplus/api-reference/document-normalizer-module.html
---

# CDocumentNormalizerModule

The `CDocumentNormalizerModule` class defines general functions in the document normalizer module.

## Definition

*Namespace:* dynamsoft::ddn

*Assembly:* DynamsoftDocumentNormalizer

```cpp
class CDocumentNormalizerModule 
```

## Methods Summary

| Method                                                        | Description                                            |
| ------------------------------------------------------------- | ------------------------------------------------------ |
| [GetVersion](#getversion)                                     | Returns the version of the document normalizer module. |
| [CreateNormalizedImageElement](#createnormalizedimageelement) | Create a Normalized Image Element object.              |
| [CreateDetectedQuadElement](#createdetectedquadelement)       | Create a Detected Quad Element object.                 |

## GetVersion

Returns the version of the document normalizer module.

```cpp
static const char* GetVersion();
```

**Parameters**

None.

**Return Value**

Returns a const char pointer representing the version of the document normalizer module.

## CreateNormalizedImageElement

Create a Normalized Image Element object.

```cpp
static intermediate_results::CNormalizedImageElement* CreateNormalizedImageElement();
```

**Parameters**

None.

**Return Value**

Returns an instance of CNormalizedImageElement.

## CreateDetectedQuadElement

Create a Detected Quad Element object.

```cpp
static intermediate_results::CDetectedQuadElement* CreateDetectedQuadElement();
```

**Parameters**

None.

**Return Value**

Returns an instance of CDetectedQuadElement.
