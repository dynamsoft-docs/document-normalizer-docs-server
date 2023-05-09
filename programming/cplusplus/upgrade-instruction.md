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

### Update the Included .h .lib & .dll file

Since the SDK architecture is changed, you have to change you code for including the headers, libs and DLLs. You can use the following code to replace your previous code.

```cpp
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

Put the following **.dll** files in your lib:

x64:

* DynamsoftCaptureVisionRouterx64.dll
* DynamsoftCorex64.dll
* DynamsoftDocumentNormalizerx64.dll
* DynamsoftImageProcessingx64.dll
* DynamsoftLicensex64.dll
* DynamsoftUtilityx64.dll

x86:

* DynamsoftCaptureVisionRouterx86.dll
* DynamsoftCorex86.dll
* DynamsoftDocumentNormalizerx86.dll
* DynamsoftImageProcessingx86.dll
* DynamsoftLicensex86.dll
* DynamsoftUtilityx86.dll

### Migrate from Class CDocumentNormalizer to Class CCaptureVisionRouter

Class `CCaptureVisionRouter` is added to replace class `CDocumentNormalizer`. Class `CCaptureVisionRouter` APIs includes the following features:

* Retrieve images
* Update templates and configure settings
* Implement document detecting or normalizing
* Dispatch the results

### Templates

The template system is upgraded. The template you used for the previous version can't be directly recognized by the new version. Please go to [this page]() to upgrade your template.

### Update Your Image Document Scanning Codes

#### Single Image Document Scanning

Since class `CDocumentNormalizer` is replaced with class `CCaptureVisionRouter`. You have to use the following `Capture` APIs instead of the `Detect/Normalize` APIs:

```cpp
// Capture from a file.
CCapturedResultArray* Capture(const char* filePath, const char* templateName="");
// Capture from a file in memory.
CCapturedResultArray* Capture(const unsigned char *fileBytes, int fileSize, const char* templateName="");
// Capture from a CImageData object.
CCapturedResult* Capture(const CImageData* pImageData, const char* templateName="");
```

#### Batch Image Document Scanning

DCV architecture allows you to set a folder as an image source to fetch image from. To use this feature, you have to set `DirectoryFetcher` as the input via class `CCaptureVisionRouter`.

```cpp
int main()
{
   CCaptureVisionRouter cvr;
 
   CDirectoryFetcher fetcher;
   // Replace the following directory path with your directory path:
   fetcher.SetDirectory("C:\\my-directory-folder\\");
   cvr.SetInput(&fetcher);
}
```

>Note: creating multiple `CCaptureVisionRouter` instances might cause crash bugs. Multi-thread processing is internally implemented. As a result you don't need to create multi-thread code by yourself.

### Update Your Video Streaming Document Scanning Codes

`CImageSourceAdapter` is added to replace the `FrameDecodeingParameters` and the previous video methods. The following steps shows how to implement video streaming document scanning with `CImageSourceAdapter`:

```cpp
class MyImageSource : public CImageSourceAdapter 
{
  // Add code to implement CImageSourceAdapter
};
int main()
{
  MyImageSource source;
  cvr.SetInput(&source);
}
```

>Note: creating multiple `CCaptureVisionRouter` instances might cause crash bugs. Multi-thread processing is internally implemented. As a result you don't need to create multi-thread code by yourself.

### Result Obtaining

If you are using batch image scanning or video streaming scanning, you have to register a `CCapturedResultReceiver` to receive the quad detecting and document normalizing results.

If you are using `Capture` APIs to process a single image, the quad detecting and document normalizing results are still available from the return value of the `Capture` APIs.