---
title: Upgrade Instructions - Dynamsoft Document Normalizer C++ Edition
keywords: c++, cplusplus, upgrade
description: This page introduces how to upgrade Dynamsoft Document Normalizer
needAutoGenerateSidebar: false
permalink: /programming/cplusplus/upgrade-instruction.html
---

# How to Upgrade

## From version 1.x to 2.x

`DynamsoftDocumentNormalizer` SDK has been refactored to integrate with `DynamsoftCaptureVision (DCV)` architecture. To upgrade from version 1.x to 2.x, we recommend you to follow the [`User Guide`](user-guide/getting-started.md) and re-write your codes.

Here are some of the main actions you may take:

### Update the Included Headers and Linked Libraries

Since the SDK architecture is changed, you have to change your code for including the headers, linking the libraries. You can use the following code to replace your previous code.

```cpp
#include "[INSTALLATION FOLDER]/Include/DynamsoftCaptureVisionRouter.h"

using namespace std;
using namespace dynamsoft::license;
using namespace dynamsoft::cvr;
using namespace dynamsoft::ddn;
using namespace dynamsoft::utility;

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

Put the following **.dll/.so** files in your executable path:

* Windows
  * x64:
    * DynamsoftDocumentNormalizerx64.dll
    * DynamsoftCaptureVisionRouterx64.dll
    * DynamsoftCorex64.dll
    * DynamsoftImageProcessingx64.dll
    * DynamsoftLicensex64.dll
    * DynamsoftUtilityx64.dll
  * x86:
    * DynamsoftDocumentNormalizerx86.dll
    * DynamsoftCaptureVisionRouterx86.dll
    * DynamsoftCorex86.dll
    * DynamsoftImageProcessingx86.dll
    * DynamsoftLicensex86.dll
    * DynamsoftUtilityx86.dll

* Linux
  * x64:
    * libDynamsoftDocumentNormalizer.so
    * libDynamsoftCaptureVisionRouter.so
    * libDynamsoftCore.so
    * libDynamsoftImageProcessing.so
    * libDynamsoftLicense.so
    * libDynamsoftUtility.so

### Migrate from Class CDocumentNormalizer to Class CCaptureVisionRouter

Class `CCaptureVisionRouter` is added to replace class `CDocumentNormalizer`. The APIs can be migrated as following mapping:

| v1.x API | v2.x API |
| --- | --- |
| class dynamsoft::ddn::CDocumentNormalizer | class dynamsoft::cvr::CCaptureVisionRouter |
| DetectQuad()<br>Normalize() | [`Capture()`]({{ site.dcv_cpp_api }}capture-vision-router/single-file-processing.md#capture) |
| InitRuntimeSettingsFromString()<br>InitRuntimeSettingsFromFile()<br>OutputRuntimeSettingsToString()<br>OutputRuntimeSettingsToFile() | [`InitSettings()`]({{ site.dcv_cpp_api }}capture-vision-router/settings.html#initsettings)<br>[`InitSettingsFromFile()`]({{ site.dcv_cpp_api }}capture-vision-router/settings.html#initsettingsfromfile)<br>[`OutputSettings()`]({{ site.dcv_cpp_api }}capture-vision-router/settings.html#outputsettings)<br>[`OutputSettingsToFile()`]({{ site.dcv_cpp_api }}capture-vision-router/settings.html#outputsettingstofile) |
| class dynamsoft::ddn::CDetectedQuadResultArray<br>class dynamsoft::ddn::CNormalizedImageResult | [`class dynamsoft::basic_structures::CCapturedResult`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result.html) |

### Convert Parameter Templates

The parameter system is restructured and the template you used for v1.x can't be directly recognized by the new version. Please <a href="https://www.dynamsoft.com/company/customer-service/#contact" target="_blank">contact us</a> to upgrade your parameter template.

### Update Your Codes

#### Single Image Processing

Since class `CDocumentNormalizer` is replaced with class `CCaptureVisionRouter`. You have to use the following `Capture` APIs instead of the `DetectQuad` and
`Normalize` APIs:

```cpp
// Capture from a file.
CCapturedResult* Capture(const char* filePath, const char* templateName="");
// Capture from a file in memory.
CCapturedResult* Capture(const unsigned char *fileBytes, int fileSize, const char* templateName="");
// Capture from a CImageData object.
CCapturedResult* Capture(const CImageData* pImageData, const char* templateName="");
```

#### Batch Image Processing

DCV architecture allows you to set a folder as an image source to fetch image from. To use this feature, you have to set `CDirectoryFetcher` as the input via class `CCaptureVisionRouter`.

```cpp
int main()
{
   CCaptureVisionRouter *cvr = new CCaptureVisionRouter;
   // Create a CDirectoryFetcher instance and set is as the input of cvr
   CDirectoryFetcher *fetcher = new CDirectoryFetcher;
   // Replace the following directory path with your directory path:
   fetcher->SetDirectory("C:\\my-directory-folder\\");
   cvr->SetInput(fetcher);
   // Create a CCapturedResultReceiver instance 
   CCapturedResultReceiver *capturedReceiver = new MyCapturedResultReceiver;
   cvr->AddResultReceiver(capturedReceiver);
   // Start capturing
   errorCode = cvr->StartCapturing(CPresetTemplate::PT_DETECT_AND_NORMALIZE_DOCUMENT, true, errorMsg, 512);
}
```

### Update Your Video Streaming Processing Codes

`CImageSourceAdapter` is added to replace the `FrameDecodeingParameters` and the previous video methods. The following steps shows how to implement video streaming detecting with `CImageSourceAdapter`:

```cpp
class MyImageSource : public CImageSourceAdapter 
{
  // Add code to implement CImageSourceAdapter
};
int main()
{
  MyImageSource *source = new MyImageSource;
  cvr->SetInput(source);
}
```

### Result Obtaining

If you are using batch image or video streaming processing APIs, you have to register a `CCapturedResultReceiver` to receive the final results.

If you are using `Capture` APIs to process a single image, the boundary detecting or document normalizing results are still available from the return value of the `Capture` APIs.