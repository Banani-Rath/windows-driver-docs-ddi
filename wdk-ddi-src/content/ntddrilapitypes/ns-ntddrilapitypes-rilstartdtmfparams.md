---
UID: NS:ntddrilapitypes.RILSTARTDTMFPARAMS
title: RILSTARTDTMFPARAMS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilstartdtmfparams.htm
old-project: netvista
ms.assetid: 3837fcee-7b94-464f-904c-c6eaa1002620
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: RILSTARTDTMFPARAMS, RILSTARTDTMFPARAMS, *LPRILSTARTDTMFPARAMS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddrilapitypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: RILSTARTDTMFPARAMS
req.alt-loc: ntddrilapitypes.h
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
req.typenames: RILSTARTDTMFPARAMS, *LPRILSTARTDTMFPARAMS
---

# RILSTARTDTMFPARAMS structure



## -description
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.



## -syntax

````
typedef struct _RILSTARTDTMFPARAMS {
  DWORD  dwExecutor;
  char   ch;
} RILSTARTDTMFPARAMS, RILSTARTDTMFPARAMS;
````


## -struct-fields

### -field dwExecutor


### -field ch


## -remarks
