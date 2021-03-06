---
UID: NF:ntintsafe.RtlUIntToUInt8
title: RtlUIntToUInt8 function
author: windows-driver-content
description: Converts a value of type UINT to a value of type UINT8.
old-location: kernel\rtluinttouint8.htm
old-project: kernel
ms.assetid: 39D4AE72-EF60-455E-A7C2-F2896E304897
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: RtlUIntToUInt8
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntintsafe.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: RtlUIntToUInt8
req.alt-loc: Ntintsafe.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
req.typenames: PUBLIC_OBJECT_TYPE_INFORMATION, *PPUBLIC_OBJECT_TYPE_INFORMATION
---

# RtlUIntToUInt8 function



## -description
Converts a value of type <b>UINT</b> to a value of type <b>UINT8</b>.



## -syntax

````
NTSTATUS RtlUIntToUInt8(
  _In_  UINT  uOperand,
  _Out_ UINT8 *pui8Result
);
````


## -parameters

### -param uOperand [in]

The value to be converted.


### -param pui8Result [out]

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns STATUS_INTEGER_OVERFLOW and this parameter is not valid.


## -remarks
This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

This function uses the following alternate name:</p>