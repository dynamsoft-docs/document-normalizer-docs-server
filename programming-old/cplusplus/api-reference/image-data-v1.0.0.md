---
layout: default-layout
title: CImageData Class
description: This page shows CImageData class definition of Dynamsoft Document Normalizer SDK C++ Edition.
keywords: CImageData, api reference
permalink: /programming/cplusplus/api-reference/image-data-v1.0.0.html
---

# CImageData

Stores the image data.  

```cpp
class dynamsoft::core::CImageData
```  

| Method               | Description |
|----------------------|-------------|
| [`CImageData`](#cimagedata) | Constructor of `CImageData` class. |
| [`CImageData`](#cimagedata-1) | Constructor of `CImageData` class. |
| [`~CImageData`](#cimagedata-2) | Destructor of `CImageData` class. |
| [`GetBytes`](#getbytes) | Get the image data content in a byte array. |
| [`GetBytesLength`](#getbyteslength) | Get the length of the image data byte array. |
| [`GetWidth`](#getwidth) | Get the width of the image in pixels. |
| [`GetHeight`](#getheight) | Get the height of the image in pixels. |
| [`GetStride`](#getstride) | Get the stride (or scan width) of the image. |
| [`GetImagePixelFormat`](#getimagepixelformat) | Get the image pixel format used in the image byte array. |

## CImageData()

Constructor of a `CCImageData` class.

```cpp
dynamsoft::core::CImageData::CImageData()

dynamsoft::core::CImageData::CImageData(int bytesLength, unsigned char* bytes, int width, int height, int stride, ImagePixelFormat format)
```

**Parameters**  
`[in] bytesLength` The length of the image data byte array.

`[in] bytes` The image data content in a byte array.

`[in] width` The the width of the image in pixels.

`[in] height` The the height of the image in pixels.

`[in] stride` The stride (or scan width) of the image.

`[in] format` The image pixel format used in the image byte array.

## ~CImageData()

Destructor of a `CCImageData` class.

```cpp
dynamsoft::core::CImageData::~CImageData()
```

## GetBytes

Get the image data content in a byte array.

```cpp
const unsigned char* GetBytes()
```

## GetBytesLength

Get the length of the image data byte array.

```cpp
int GetBytesLength()
```

## GetWidth

Get the width of the image in pixels.  

```cpp
int GetWidth()
```

## GetHeight

Get the height of the image in pixels.  

```cpp
int GetHeight()
```

## GetStride

Get the stride (or scan width) of the image.

```cpp
int GetStride()
```

## GetImagePixelFormat

Get the image pixel format used in the image byte array.

```cpp
ImagePixelFormat GetImagePixelFormat()
```

**See Also**

[ImagePixelFormat]({{ site.enumerations }}image-pixel-format.html?src=cpp)
