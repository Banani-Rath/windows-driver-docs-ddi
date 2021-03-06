---
UID: NC:d3d12umddi.PFND3D12DDI_CALCPRIVATEVIDEODECODERHEAPSIZE_0032
title: PFND3D12DDI_CALCPRIVATEVIDEODECODERHEAPSIZE_0032
author: windows-driver-content
description: Used to calculate the size of a video decoder heap.
old-location: display\pfnd3d12ddi_calcprivatevideodecoderheapsize_0032_.htm
old-project: display
ms.assetid: BEC5D467-87B1-4AED-9DB8-A3D94A373464
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: _D3D11_1DDI_GETCAPTUREHANDLEDATA, D3D11_1DDI_GETCAPTUREHANDLEDATA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d12umddi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: PFND3D12DDI_CALCPRIVATEVIDEODECODERHEAPSIZE_0032
req.alt-loc: d3d12umddi.h
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
req.typenames: D3D11_1DDI_GETCAPTUREHANDLEDATA
---

# PFND3D12DDI_CALCPRIVATEVIDEODECODERHEAPSIZE_0032 callback



## -description
Used to calculate the size of a video decoder heap.



## -prototype

````
SIZE_T APIENTRY* PFND3D12DDI_CALCPRIVATEVIDEODECODERHEAPSIZE_0032(
             D3D12DDI_HDEVICE                           hDrvDevice,
  _In_ const D3D12DDIARG_CREATE_VIDEO_DECODER_HEAP_0032 *pArgs
);
````


## -parameters

### -param hDrvDevice 

The hardware device being processed.


### -param pArgs [in]

The arguments used to create a video decoder heap.


## -returns
Returns the size of the heap in bytes.


## -remarks
