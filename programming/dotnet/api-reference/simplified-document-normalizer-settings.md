---
layout: default-layout
title: SimplifiedDocumentNormalizerSettings Class - Dynamsoft Document Normalizer Module .NET Edition API Reference
description: Definition of the SimplifiedDocumentNormalizerSettings class in Dynamsoft Document Normalizer Module .NET Edition.
keywords: class, .NET, SimplifiedDocumentNormalizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# SimplifiedDocumentNormalizerSettings

The `SimplifiedDocumentNormalizerSettings` class contains settings for document normalization. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

```csharp
typedef class SimplifiedDocumentNormalizerSettings
{
    GrayscaleTransformationMode grayscaleTransformationModes[];     
    GrayscaleEnhancementMode grayscaleEnhancementModes[];     
    ImageColourMode colourMode;    
    int pageSize[];    
    int brightness;    
    int contrast;    
    int maxThreadsInOneTask;    
    int scaleDownThreshold;    
} SimplifiedDocumentNormalizerSettings;

```

## Attributes Summary

| Attribute | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *GrayscaleTransformationMode[]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *GrayscaleEnhancementMode[]* |
| [`colourMode`](#colourmode) | *int* |
| [`pageSize`](#pagesize) | *int[]* |
| [`brightness`](#brightness) | *int* |
| [`contrast`](#contrast) | *int* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* |

### grayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration `GrayscaleTransformationMode`. View the reference page of <a href="{{ site.dcv_enumerations}}core/grayscale-transformation-mode.html?lang=dotnet" target="_blank">`GrayscaleTransformationMode`</a> for more detail about grayscale transformation modes.

```csharp
GrayscaleTransformationMode grayscaleTransformationModes[];
```

### grayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration `GrayscaleEnhancementMode`. View the reference page of <a href="{{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html?lang=dotnet" target="_blank">`GrayscaleEnhancementMode`</a> for more detail about grayscale enhancement modes.

```csharp
GrayscaleEnhancementMode grayscaleEnhancementModes[];
```

### colourMode

Set the output image colour mode.

```csharp
ImageColourMode colourMode;
```

**Value Range**

"ICM_BINARY", "ICM_GRAYSCALE", "ICM_COLOUR"

**Default value**

"ICM_COLOUR"

### pageSize

Set the page size (width by height in pixels) of the normalized image.

```csharp
int pageSize[];
```


### brightness

Set the brightness of the normalized image.

```csharp
int brightness;
```

**Value Range**

[-100,100]

**Default value**

0

### contrast

Set the contrast of the normalized image.

```csharp
int contrast   
```

**Value Range**

[-100,100]

**Default value**

0

### maxThreadsInOneTask

Set the maximum available threads count in one document normalization task.

```csharp
int maxThreadsInOneTask;
```

**Value Range**

[1, 256]

**Default value**

4

### scaleDownThreshold

Sets the threshold for the image shrinking.

```csharp
int scaleDownThreshold;
```

**Value Range**

[512, 0x7fffffff]

**Default Value**

2300

**Remarks**

If the shorter edge size is larger than the given threshold value, the library will calculate the required height and width of the barcode image and shrink the image to that size before detection. Otherwise, the library will perform document detection on the original image.

