---
layout: default-layout
title: ImageColourMode - Dynamsoft Document Normalizer Enumerations
description: "Explore ImageColourMode values in Dynamsoft Document Normalizer C++ API and learn how they define status, configuration, and processing behavior for modern web."
keywords: Mapping status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageColourMode
---

# Enumeration ImageColourMode

`ImageColourMode` describes the output colour mode of the normalized image.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum ImageColourMode
{
    /** Output image in colour mode. */
    ICM_COLOUR = 0,    
    /** Output image in grayscale mode. */
    ICM_GRAYSCALE = 1,     
    /** Output image in binary mode. */
    ICM_BINARY = 2
} ImageColourMode;
```