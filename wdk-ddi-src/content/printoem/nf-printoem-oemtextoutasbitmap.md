---
UID: NF:printoem.OEMTextOutAsBitmap
title: OEMTextOutAsBitmap function
author: windows-driver-content
description: OEMTextOutAsBitmap function
old-location: print\oemtextoutasbitmap.htm
old-project: print
ms.assetid: 37bf1cbe-9200-4d3e-b5e6-746f18293c1a
ms.author: windowsdriverdev
ms.date: 1/8/2018
ms.keywords: OEMTextOutAsBitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: printoem.h
req.include-header: Printoem.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: OEMTextOutAsBitmap
req.alt-loc: printoem.h
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
req.typenames: STDVARIABLEINDEX
req.product: Windows 10 or later.
---

# OEMTextOutAsBitmap function



## -description

## -syntax

````
BOOL APIENTRY OEMTextOutAsBitmap(
   SURFOBJ  *pso,
   STROBJ   *pstro,
   FONTOBJ  *pfo,
   CLIPOBJ  *pco,
   RECTL    *prclExtra,
   RECTL    *prclOpaque,
   BRUSHOBJ *pboFore,
   BRUSHOBJ *pboOpaque,
   POINTL   *pptlOrg,
   MIX      mix
);
````


## -parameters

### -param pso 


### -param pstro 


### -param pfo 


### -param pco 


### -param prclExtra 


### -param prclOpaque 


### -param pboFore 


### -param pboOpaque 


### -param pptlOrg 


### -param mix 


## -remarks
