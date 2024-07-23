---
layout: default-layout
title: struct SimplifiedDocumentNormalizerSettings - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the SimplifiedDocumentNormalizerSettings struct of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: struct, c++, SimplifiedDocumentNormalizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ SimplifiedDocumentNormalizerSettings Struct
---

# SimplifiedDocumentNormalizerSettings

The `SimplifiedDocumentNormalizerSettings` struct contains settings for document normalization. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

```cpp
typedef struct tagSimplifiedDocumentNormalizerSettings
{
    GrayscaleTransformationMode grayscaleTransformationModes[8];     
    GrayscaleEnhancementMode grayscaleEnhancementModes[8];     
    ImageColourMode colourMode;    
    int pageSize[2];    
    int brightness;    
    int contrast;    
    int maxThreadsInOneTask;    
    int scaleDownThreshold;    
    char reserved[512];
} SimplifiedDocumentNormalizerSettings;

```

## Attributes Summary

| Attribute | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *GrayscaleTransformationMode[8]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *GrayscaleEnhancementMode[8]* |
| [`colourMode`](#colourmode) | *int* |
| [`pageSize`](#pagesize) | *int[2]* |
| [`brightness`](#brightness) | *int* |
| [`contrast`](#contrast) | *int* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* |
| [`reserved`](#reserved) | *char[508]* |

### grayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration `GrayscaleTransformationMode`. View the reference page of <a href="{{ site.dcv_enumerations}}core/grayscale-transformation-mode.html?src=cpp&&lang=cpp" target="_blank">`GrayscaleTransformationMode`</a> for more detail about grayscale transformation modes.

```cpp
GrayscaleTransformationMode grayscaleTransformationModes[8];
```

### grayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration `GrayscaleEnhancementMode`. View the reference page of <a href="{{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html?src=cpp&&lang=cpp" target="_blank">`GrayscaleEnhancementMode`</a> for more detail about grayscale enhancement modes.

```cpp
GrayscaleEnhancementMode grayscaleEnhancementModes[8];
```

### colourMode

Set the output image colour mode.

```cpp
ImageColourMode colourMode;
```

**Value Range**

"ICM_BINARY", "ICM_GRAYSCALE", "ICM_COLOUR"

**Default value**

"ICM_COLOUR"

### pageSize

Set the page size (width by height in pixels) of the normalized image.

```cpp
int pageSize[2];
```


### brightness

Set the brightness of the normalized image.

```cpp
int brightness;
```

**Value Range**

[-100,100]

**Default value**

0

### contrast

Set the contrast of the normalized image.

```cpp
int contrast   
```

**Value Range**

[-100,100]

**Default value**

0

### maxThreadsInOneTask

Set the maximum available threads count in one document normalization task.

```cpp
int maxThreadsInOneTask;
```

**Value Range**

[1, 256]

**Default value**

4

**Remarks**

To keep a balance between speed and quality, the library concurrently runs four different threads by default.

### scaleDownThreshold

Sets the threshold for the image shrinking.

```cpp
int scaleDownThreshold;
```

**Value Range**

[512, 0x7fffffff]

**Default Value**

2300

**Remarks**

If the shorter edge size is larger than the given threshold value, the library will calculate the required height and width of the barcode image and shrink the image to that size before detection. Otherwise, the library will perform document detection on the original image.

### reserved

Reserved for future use.

```cpp
char reserved[508];
```
