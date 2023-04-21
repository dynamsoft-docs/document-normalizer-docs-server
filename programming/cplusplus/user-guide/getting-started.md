---
layout: default-layout
title: User Guide for C++ Language
keywords: user guide, hello world
description: Dynamsoft Document Normalizer - User Guide for C++ Language
---

# Document Normalizer in C++ - User Guide

In this guide, you will learn step by step on how to build a document normalization application with Dynamsoft Document Normalizer SDK using C++ language.

> Read more on [Dynamsoft Document Normalizer Features](https://www.dynamsoft.com/document-normalizer/docs/introduction/index.html)

- [Installation](#installation)
- [Build Your First Application](#build-your-first-application)
  - [Create a New Project](#create-a-new-project)
  - [Include the Library](#include-the-library)
  - [Initialize a Capture Vision Router Instance](#initialize-a-capture-vision-router-instance)
  - [Detect and Save the Normalized Document](#detect-and-save-the-normalized-document)
  - [Build and Run the Project](#build-and-run-the-project)
- [Process Multiple Images](#process-multiple-images)
  - [Add an Image Source as the Input](#add-an-image-source-as-the-input)
  - [Add a Result Receiver as the Output](#add-a-result-receiver-as-the-output)
  - [Add an Object to Listener to the Status of the Image Source](#add-an-object-to-listener-to-the-status-of-the-image-source)
  - [Start the Process](#start-the-process)
  - [Build and Run the Project Again](#build-and-run-the-project-again)

## Installation

If you haven't downloaded the SDK yet, <a href="https://download2.dynamsoft.com/ddn/dynamsoft-document-normalizer-c_cpp-2.0.0.zip">download the `C/C++ Package`</a> now and unpack the package into a directory of your choice.

> For this tutorial, we unpack it to a pseudo directory `[INSTALLATION FOLDER]`, change it to your unpacking path for the following content.

> To find out whether your environment is supported, read the [System Requirements](https://www.dynamsoft.com/document-normalizer/docs/server/programming/cplusplus/#system-requirements).

## Build Your First Application

Let's start by creating a console application which demonstrates how to use the minimum code to detect and normalize a document from an picture of it.

> You can <a href="https://github.com/Dynamsoft/document-normalizer-c-cpp-samples/tree/main/Samples/C%2B%2B/HelloWorld" target="_blank">download the entire source code from here</a>.

### Create a New Project

- For Windows

1. Open Visual Studio. Go to "File > New > Project..." or click "Create a new project" on the starting page, choose "Console App", create a new Empty Project and set the Project name as `DDNCPPSample`.

2. Add a new source file named `DDNCPPSample.cpp` into the project.

- For Linux

1. Create a new source file named `DDNCPPSample.cpp` and place it into the folder `[INSTALLATION FOLDER]/Samples`.

### Include the Library

1. Add headers and libs in `DDNCPPSample.cpp`.

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
            #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x64/DynamsoftCaptureVisionx64.lib")
        #else
            #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x86/DynamsoftLicensex86.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x86/DynamsoftCaptureVisionx86.lib")
        #endif
    #endif
    ```

### Initialize a Capture Vision Router Instance

1. Initialize the license key.

    ```cpp
    char errorMsg1[256];
    CLicenseManager::InitLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", errorMsg1, 256);
    ```

    > The string "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" here is a free public trial license. Note that network connection is required for this license to work. When it expires, you can request a 30-day free trial license from the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=guide&product=ddn&package=desktop" target="_blank">Customer Portal</a>.

2. Create an instance of Capture Vision Router.

    ```cpp
    CCaptureVisionRouter cvr;
    ```

### Detect and Save the Normalized Document

1. Apply normalization for an image file.

    ```cpp
	CCapturedResultArray* results = cvr.Capture("[INSTALLATION FOLDER]/Images/sample-image.jpg", PresetTemplate::PT_DETECT_AND_NORMALIZE_DOCUMENT);
	/*
	* results is an Array of CCapturedResult objects, each object is the result of an image.
	* In our case, there is only one image, so the first result is the result for it.
	*/
	const CCapturedResult* result = results->GetResult(0);
	int count = result->GetCount();
	const CNormalizedImageResultItem* normalizedImage = NULL;
	/*
	* There can be multiple types of result items per image.
	* We check each of these items until we find the normalized image.
	*/
	for (int i = 0; i < count; i++) {
		const CCapturedResultItem* item = result->GetItem(0);
		CapturedResultItemType type = item->GetType();
		if (type | CapturedResultItemType::CRIT_NORMALIZED_IMAGE) {
			normalizedImage = dynamic_cast<const ddn::CNormalizedImageResultItem*>(item);
		}
	}
    ```

2. Save the normalized result as an image file.

    ```cpp
	/*
	* We check whether the normalized image exists.
	* If yes, we save the image to the disk.
	*/
	if (normalizedImage != NULL)
	{
		const CImageData* img = normalizedImage->GetImageData();
		string filePath = "[INSTALLATION FOLDER]/results/normalizedResult.png";
		int saveReturnCode = normalizedImage->SaveToFile(filePath.c_str());
		if (saveReturnCode == 0){
			std::cout << "Normalized image saved!\n";
            }
	}
	else {
		std::cout << "Normalization failed!\n";
	}    
    ```
> Note:
> 
> Please change all `[INSTALLATION FOLDER]` in above code snippet to your unpacking path.

### Build and Run the Project

- For Windows

1. In Visual Studio, set the solution to build as Release\|x64.

2. Build the project to generate program `DDNCPPSample.exe`.

3. Copy **ALL** `*.dll` files under `[INSTALLATION FOLDER]\Lib\Windows\x64` to the same folder as the `DDNCPPSample.exe` ("[PROJECT FOLDER]\DDNCPPSample\x64\Debug").

4. Run the program `DDNCPPSample.exe`.

> The SDK supports both x86 and x64, please set the platform based on your needs.

- For Linux

1. Open a terminal and change to the target directory where `DDNCPPSample.cpp` is located. Build the sample:

    ```bash
    g++ -o DDNCPPSample DDNCPPSample.cpp -lDynamsoftCore -lDynamsoftDocumentNormalizer -L ../Lib/Linux -Wl,-rpath=../Lib/Linux -std=c++11
    ```

2. Run the program `DDNCPPSample`.

    ```bash
    ./DDNCPPSample
    ```

> You can <a href="https://github.com/Dynamsoft/document-normalizer-c-cpp-samples/tree/main/Samples/C%2B%2B/HelloWorld" target="_blank">download the entire source code from here</a>.

## Process Multiple Images

If, instead of processing one single image, you need to process many images at once, you can follow these steps:

> These steps follow the step [Initialize a Capture Vision Router Instance](#initialize-a-capture-vision-router-instance) mentioned above.

### Add an Image Source as the Input

The class `DirectoryFetcher` is capable of converting a local directory to an image source. We will use it to connect multiple images to the image-processing engine.

1. Include the header file.

    ```cpp
    // Add the following lines
    #include "Include/DynamsoftUtility.h"
    using namespace dynamsoft::utility;
    #ifdef _WIN64
    #pragma comment(lib, "Lib/x64/DynamsoftUtilityx64.lib")
    #pragma comment(lib, "Lib/x64/DynamsoftCorex64.lib")
    #else
    #pragma comment(lib, "Lib/x86/DynamsoftUtilityx86.lib")
    #pragma comment(lib, "Lib/x86/DynamsoftCorex86.lib")
    #endif
    ```

2. Create a `DirectoryFetcher` object and use it as the image source.

    ```cpp
	CDirectoryFetcher fetcher;
	fetcher.SetDirectory("[THE DIRECTORY THAT HOLDS THE IMAGES]");
	cvr.SetInput(&fetcher);
    ```

### Add a Result Receiver as the Output

1. Define the receiver class.

    ```cpp
    class MyCapturedResultReceiver : public CCapturedResultReceiver {
        void OnNormalizedImagesReceived(const CNormalizedImagesResult* pResult) {
            const CFileImageTag* fileImageTag = dynamic_cast<const CFileImageTag*>(pResult->GetSourceImageTag());
            string originalFilePath = fileImageTag->GetFilePath();
            int count = pResult->GetCount();
            /**
            * All these result items are of the type CNormalizedImageResultItem.
            * So we can save each result as an image.
            */
            for (int i = 0; i < count; i++) {
                const CNormalizedImageResultItem* normalizedImage = NULL;
                const CCapturedResultItem* item = pResult->GetItem(i);
                normalizedImage = dynamic_cast<const CNormalizedImageResultItem*>(item);
                if (normalizedImage != NULL)
                {
                    const CImageData* img = normalizedImage->GetImageData();
                    /*
                     * Save the normalized image to the same directory of the original images to make it easier to compare the two.
                     */
                    string filePath = originalFilePath.substr(0, originalFilePath.find_last_of(".")) + "-result-" + std::to_string(i) + ".png";
                    int saveReturnCode = normalizedImage->SaveToFile(filePath.c_str());
                    if (saveReturnCode == 0) {
                        std::cout << originalFilePath << ": Normalized image " << std::to_string(i) << " saved!\n";
                    }
                }
            }
        }
    };
    ```

2. Create a receiver object and set it as the output.

    ```cpp
	MyCapturedResultReceiver capturedReceiver;
	cvr.AddResultReceiver(&capturedReceiver);
    ```

### Add an Object to Listener to the Status of the Image Source

1. Define the listener class.

    ```cpp
    class MyImageSourceAdapterStateListener : public virtual CImageSourceAdapterStateListener {
    public:
        CCaptureVisionRouter* cvr = NULL;
        void OnImageSourceAdapterStateChanged(ImageSourceState state) {
            if (state == ISS_EXHAUSTED) {
                cvr->StopCapturing();
            }
        }
    };
    ```

2. Create a listener object and connect it to the image source

    ```cpp
    MyImageSourceAdapterStateListener listener;
	listener.cvr = &cvr;
	cvr.AddImageSourceAdapterStateListener(&listener);
    ```

### Start the Process

Call the method `StartCapturing()` to start processing all the images in the specified folder.

```cpp
char error2[512];
int ret2 = cvr.StartCapturing(PresetTemplate::PT_DETECT_AND_NORMALIZE_DOCUMENT, true, error2, 512);        
```

During the process, the callback function `OnNormalizedImagesReceived()` is triggered each time an image finishes processing. After all images are processed, the listener function `OnImageSourceAdapterStateChanged()` will return the image source state as `ISS_EXHAUSTED` and the process is stopped with the method `StopCapturing()`.

### Build and Run the Project Again

Please refer to [Build and Run the Project](#build-and-run-the-project).
