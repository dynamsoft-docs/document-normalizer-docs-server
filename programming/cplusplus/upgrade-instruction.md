---
title: Upgrade Instructions - Dynamsoft Document Normalizer C++ Edition
keywords: c++, cplusplus, upgrade
description: This page introduces how to upgrade Dynamsoft Document Normalizer
needAutoGenerateSidebar: false
permalink: /programming/cplusplus/upgrade-instruction.html
---

# How to Upgrade

## From 1.x to 2.x

`DynamsoftDocumentNormalizer` SDK has been refactored to integrate with `DynamsoftCaptureVision (DCV)` architecture. Notice the following break changes when upgrading your SDK.

### Update the Included Headers, libs & DLLs

Since the SDK architecture is changed, you have to change you code for including the headers, libs and DLLs. You can use the following code to replace your previous code.

```cpp
#include <iostream>
#include <string>
#include "[INSTALLATION FOLDER]/Include/DynamsoftLicense.h"
#include "[INSTALLATION FOLDER]/Include/DynamsoftCaptureVisionRouter.h"
#include "[INSTALLATION FOLDER]/Include/DynamsoftDocumentNormalizer.h"

using namespace std;
using namespace dynamsoft::license;
using namespace dynamsoft::cvr;
using namespace dynamsoft::ddn;

#if defined(_WIN64) || defined(_WIN32)
    #ifdef _WIN64
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x64/DynamsoftLicensex64.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x64/DynamsoftCaptureVisionRouterx64.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x64/DynamsoftDocumentNormalizerx64.lib")
    #else
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x86/DynamsoftLicensex86.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x86/DynamsoftCaptureVisionRouterx86.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x86/DynamsoftDocumentNormalizerx86.lib")
    #endif
#endif
```

### Replace CDocumentNormalizer Class with CCaptureVisionClass

In 2.0 version, we added `CCaptureVisionRouter` class to retrieve images, configure settings, implement document detection/normalization and dispatch the results to the receivers.

#### Replace Detect/Normalize APIs with Capture APIs

#### Replace PublicRuntimeSettings with SimplifiedSettings

### Processing a Set of Image Files

DCV architecture allows you to set a folder as an image source to fetch image from. To use this feature, you have to set `DirectoryFetcher` as the input via CaptureVisionRouter class. When using `DirectoryFetcher` as input, the multi-thread is internally allocated. As a result, you don't need to write code for multi-thread configurations.

The following code snippet shows how to setup `DirectoryFetcher`:

```cpp
CCaptureVisionRouter cvr;

CDirectoryFetcher fetcher;
fetcher.SetDirectory("C:\\cpp-projects\\HelloWorld\\Images\\");
cvr.SetInput(&fetcher);
```

### Templates

The template system is upgraded. The template you used for the previous version can't be directly recognized by the new version. Please go to [this page]() to upgrade your template.

### Results
