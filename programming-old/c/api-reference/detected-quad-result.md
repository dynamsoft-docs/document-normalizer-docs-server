---
layout: default-layout
title: DetectedQuadResult Struct - Dynamsoft Document Normalizer SDK C Edition
description: This page shows DetectedQuadResult struct definition of Dynamsoft Document Normalizer SDK C Edition.
keywords: Location, ConfidenceAsDocumentBoundary, DetectedQuadResult, struct
permalink: /programming/c/api-reference/detected-quad-result.html
---

# DetectedQuadResult Struct

Stores the detected quad result.

## Definition

```c
typedef struct tagDetectedQuadResult
{
    Quadrilateral *location;
    int confidenceAsDocumentBoundary;
}DetectedQuadResult, *PDetectedQuadResult;
```

### location

The location of the detected quad result.

**See Also**

[Quadrilateral](quadrilateral.md)

### confidenceAsDocumentBoundary

The confidence as document boundary of the detected quad result.
