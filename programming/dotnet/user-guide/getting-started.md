---
layout: default-layout
title: User Guide - Dynamsoft Document Normalizer SDK .NET Edition
description: This is the user guide of Dynamsoft Document Normalizer SDK .NET Edition.
keywords: user guide, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Getting Started with Dynamsoft Document Normalizer SDK .NET Edition

In this guide, you will learn step by step on how to build a document normalization application with Dynamsoft Document Normalizer SDK using C#.

- [Getting Started with Dynamsoft Document Normalizer SDK .NET Edition](#getting-started-with-dynamsoft-document-normalizer-sdk-net-edition)
  - [System Requirements](#system-requirements)
  - [Build Your First Application](#build-your-first-application)
    - [Create a New Project](#create-a-new-project)
    - [Install the NuGet Package](#install-the-nuget-package)
    - [Import the Namespace](#import-the-namespace)
    - [Initialize the License Key](#initialize-the-license-key)
    - [Create a CaptureVisionRouter Instance](#create-a-capturevisionrouter-instance)
    - [Invoke the Document Capturing](#invoke-the-document-capturing)
    - [Filter and Get Document Detection and Normalization Results](#filter-and-get-document-detection-and-normalization-results)
    - [Build and Run the Project](#build-and-run-the-project)
  - [Process Multiple Images](#process-multiple-images)
    - [Import the Additional Namespace.](#import-the-additional-namespace)
    - [Create an ImageSource as the Input](#create-an-imagesource-as-the-input)
    - [Implement a CapturedResultReceiver as the Output Listener](#implement-a-capturedresultreceiver-as-the-output-listener)
    - [Handle Capture Stoppage by Implementing a ImageSource State Listener](#handle-capture-stoppage-by-implementing-a-imagesource-state-listener)
    - [Register the Input, Output Listener and ImageSource State Listener to the CaptureVisionRouter Instance](#register-the-input-output-listener-and-imagesource-state-listener-to-the-capturevisionrouter-instance)
    - [Start the Capturing Process](#start-the-capturing-process)
    - [Build and Run the Project Again](#build-and-run-the-project-again)

## System Requirements

To find out whether your environment is supported, please read the [System Requirements]({{ site.ddn_dotnet}}index.html#system-requirements).

## Build Your First Application

Let's start by creating a console application which demonstrates how to use the minimum code to detect and normalize a document from an image file.

> You can <a href="https://github.com/Dynamsoft/document-normalizer-dotnet-samples/tree/main/Samples/HelloWorld/NormalizeAnImage" target="_blank">download the entire source code from here</a>.

### Create a New Project

Start Visual Studio or your preferred C# IDE.

Create a new C# Console Application project.

### Install the NuGet Package

In the Solution Explorer, right-click on your project and select Manage NuGet Packages.

Search for and install the `Dynamsoft.DotNet.DocumentNormalizer.Bundle` nuget package.

> If you prefer to use the offline packages, please
> 
> <a href="https://www.dynamsoft.com/document-normalizer/downloads/?utm_source=docs" target="_blank">Download the `.NET Package`</a> now and extract it into a directory of your choice.
> 
> Add the extracted `.\Dynamsoft\Packages` directory as a new package source
> 
> Install following packages from the added package source:
> * Dynamsoft.DotNet.DocumentNormalizer
> * Dynamsoft.DotNet.CaptureVisionRouter
> * Dynamsoft.DotNet.Core
> * Dynamsoft.DotNet.ImageProcessing
> * Dynamsoft.DotNet.License
> * Dynamsoft.DotNet.Utility

### Import the Namespace

Open the `Program.cs` file and add the following namespaces.

```csharp
using Dynamsoft.DDN;
using Dynamsoft.Core;
using Dynamsoft.CVR;
using Dynamsoft.License;
```

### Initialize the License Key

Open the `Program.cs` file and add the following code inside the `Main` method to initialize the license for using the SDK in the application:

```csharp
int errorCode = 1;
string errorMsg;
errorCode = LicenseManager.InitLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", out errorMsg);
if (errorCode != (int)EnumErrorCode.EC_OK && errorCode != (int)EnumErrorCode.EC_LICENSE_CACHE_USED)
    Console.WriteLine("License initialization error: " + errorMsg);
```

> The string "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" here is a free public trial license. Note that network connection is required for this license to work. When it expires, you can request a 30-day trial license via the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=guide&product=ddn&package=dotnet" target="_blank">Request a Trial License</a> link.

### Create a CaptureVisionRouter Instance

```csharp
using (CaptureVisionRouter cvr = new CaptureVisionRouter())
{
    //code for invoking the document capturing
}
```

### Invoke the Document Capturing

```csharp
using (CaptureVisionRouter cvr = new CaptureVisionRouter())
{
    string imageFile = "[PATH-TO-THE-IMAGE-FILE]";
    CapturedResult? result = cvr.Capture(imageFile, PresetTemplate.PT_DETECT_AND_NORMALIZE_DOCUMENT);
    //code for filtering and getting document detection and normalization results
}
```

> Please change the `[PATH-TO-THE-IMAGE-FILE]` to a real image file path.
> 
> Sample images are also available in the `\Dynamsoft\Resources\DocumentNormalizer\Images` directory within the downloaded `.NET package`.

### Filter and Get Document Detection and Normalization Results

```csharp
if (result == null)
{
    Console.WriteLine("No Result.");
}
else if(result.GetErrorCode() != 0)
{
    Console.WriteLine("Error: " + result.GetErrorCode() + ", " + result.GetErrorString());
}
else
{
    NormalizedImagesResult? normalizedImagesResult = result.GetNormalizedImagesResult();
    if (normalizedImagesResult != null)
    {
        NormalizedImageResultItem[] items = normalizedImagesResult.GetItems();
        Console.WriteLine("Detected and Normalized " + items.Length + " documents");
        foreach (NormalizedImageResultItem normalizedItem in items)
        {
            string outPath = "normalizedResult_" + Array.IndexOf(items, normalizedItem) + ".png";
            ImageManager imageManager = new ImageManager();
            var image = normalizedItem.GetImageData();
            if (image != null)
            {
                errorCode = imageManager.SaveToFile(image, outPath);
                if (errorCode == 0)
                {
                    Console.WriteLine("Document " + Array.IndexOf(items, normalizedItem) + " file: " + outPath);
                }
            }
        }
    }
}
```

### Build and Run the Project

Save the `Program.cs` file and then compile and run the program using your IDE (such as Visual Studio). You will see the output message in the console like

```
Detected and Normalized 1 documents
Document 1 file: normalizedResult_1.png
```

## Process Multiple Images

If, instead of processing one single image, you need to process many images at once, you can follow these steps:

> These steps follow the step [Create a CaptureVisionRouter Instance](#create-a-capturevisionrouter-instance) mentioned above.

> You can <a href="https://github.com/Dynamsoft/document-normalizer-dotnet-samples/tree/main/Samples/HelloWorld/NormalizeMultipleImages" target="_blank">download the entire source code from here</a>.

### Import the Additional Namespace.

```csharp
using Dynamsoft.Utility;
```

### Create an ImageSource as the Input

An `ImageSource` is required when crreating a multi-image processing application. You can either utilize ready-made image sources such as [`FileFetcher`]({{ site.dcv_dotnet_api }}utility/file-fetcher.html) and [`DirectoryFetcher`]({{ site.dcv_dotnet_api }}utility/directory-fetcher.html), or customize your own image source based on the base class [`ImageSourceAdapter`]({{ site.dcv_dotnet_api }}core/basic-classes/image-source-adapter.html).

In this sample, we will use the `DirectoryFetcher` to retrieve images from a local directory.

```csharp
DirectoryFetcher fetcher = new DirectoryFetcher();
fetcher.SetDirectory("[THE DIRECTORY THAT HOLDS THE IMAGES]");
```

> Please change the `[THE DIRECTORY THAT HOLDS THE IMAGES]` to full path of the directory holding image files.
> 
> Sample images are also available in the `\Dynamsoft\Resources\DocumentNormalizer\Images` directory within the downloaded `.NET package`.

### Implement a CapturedResultReceiver as the Output Listener

Create a class `MyCapturedResultReceiver` to implement the `CapturedResultReceiver` interface, and get the barocde results in `OnNormalizedImagesReceived` callback function.

```csharp
class MyCapturedResultReceiver : CapturedResultReceiver
{
    public override void OnNormalizedImagesReceived(NormalizedImagesResult result)
    {
        FileImageTag? tag = (FileImageTag?)result.GetOriginalImageTag();
        Console.WriteLine("File: " + tag.GetFilePath());
        if (result.GetErrorCode() != (int)EnumErrorCode.EC_OK)
        {
            Console.WriteLine("Error: " + result.GetErrorString());
        }
        else
        {
            NormalizedImagesResult? normalizedImagesResult = result.GetNormalizedImagesResult();
            if (normalizedImagesResult != null)
            {
                NormalizedImageResultItem[] items = normalizedImagesResult.GetItems();
                Console.WriteLine("Detected and Normalized " + items.Length + " documents");
                foreach (NormalizedImageResultItem normalizedItem in items)
                {
                    string outPath = "normalizedResult_" + Array.IndexOf(items, normalizedItem) + ".png";
                    ImageManager imageManager = new ImageManager();
                    var image = normalizedItem.GetImageData();
                    if (image != null)
                    {
                        errorCode = imageManager.SaveToFile(image, outPath);
                        if (errorCode == 0)
                        {
                            Console.WriteLine("Document " + Array.IndexOf(items, normalizedItem) + " file: " + outPath);
                        }
                    }
                }
            }
        }
        Console.WriteLine();
    }
}
```

### Handle Capture Stoppage by Implementing a ImageSource State Listener

Create a class `MyImageSourceStateListener` to implement the `IImageSourceStateListener` interface, and call StopCapturing in `OnImageSourceStateReceived` callback function when the state is `ISS_EXHAUSTED`.

```csharp
class MyImageSourceStateListener : IImageSourceStateListener
{
    private CaptureVisionRouter? cvr = null;
    public MyImageSourceStateListener(CaptureVisionRouter cvr)
    {
        this.cvr = cvr;
    }
    public void OnImageSourceStateReceived(EnumImageSourceState state)
    {
        if (state == EnumImageSourceState.ISS_EXHAUSTED)
        {
            if (cvr != null)
            {
                cvr.StopCapturing();
            }
        }
    }
}
```

### Register the Input, Output Listener and ImageSource State Listener to the CaptureVisionRouter Instance

```csharp
cvr.SetInput(fetcher);
CapturedResultReceiver receiver = new MyCapturedResultReceiver();
cvr.AddResultReceiver(receiver);
MyImageSourceStateListener listener = new MyImageSourceStateListener(cvr);
cvr.AddImageSourceStateListener(listener);
```

### Start the Capturing Process

Call the method `StartCapturing()` to start processing all the images in the specified folder.

```csharp
errorCode = cvr.StartCapturing(PresetTemplate.PT_DETECT_AND_NORMALIZE_DOCUMENT, true, out errorMsg);
if (errorCode != (int)EnumErrorCode.EC_OK)
{
    Console.WriteLine("error: " + errorMsg);
}
```

During the process, the callback function `OnNormalizedImagesReceived()` is triggered each time processing of an image is finished. After all images are processed, the listener function `OnImageSourceStateReceived()` will be triggered while the image source state is `ISS_EXHAUSTED` and the process is stopped with the method `StopCapturing()`.

### Build and Run the Project Again

Please refer to [Build and Run the Project](#build-and-run-the-project).

