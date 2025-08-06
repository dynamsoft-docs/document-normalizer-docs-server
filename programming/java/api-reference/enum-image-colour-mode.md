---
layout: default-layout
title: EnumImageColourMode - Dynamsoft Document Normalizer Java Enumerations
description: The enumeration EnumImageColourMode of Dynamsoft Document Normalizer describes the mapping status of a parsed field.
keywords: Mapping status
---

# Enumeration ImageColourMode

`EnumImageColourMode` describes the output colour mode of the normalized image.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageColourMode {
    //Output image in colour mode.
    int ICM_COLOUR = 0;    
    //Output image in grayscale mode.
    int ICM_GRAYSCALE = 1;     
    //Output image in binary mode.
    int ICM_BINARY = 2;
}
```