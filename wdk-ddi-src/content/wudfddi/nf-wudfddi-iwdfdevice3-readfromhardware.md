---
UID: NF:wudfddi.IWDFDevice3.ReadFromHardware
title: IWDFDevice3::ReadFromHardware method
author: windows-driver-content
description: The ReadFromHardware method is used internally by the framework. Do not use.
old-location: wdf\iwdfdevice3_readfromhardware.htm
old-project: wdf
ms.assetid: 19B472D0-D607-4874-ADB9-232C379B0DFD
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: IWDFDevice3, IWDFDevice3::ReadFromHardware, ReadFromHardware
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
req.alt-api: IWDFDevice3.ReadFromHardware
req.alt-loc: WUDFx.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WUDFx.dll
req.irql: 
req.typenames: *PPOWER_ACTION, POWER_ACTION
req.product: Windows 10 or later.
---

# IWDFDevice3::ReadFromHardware method



## -description
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>ReadFromHardware</b> method is used internally by the framework. Do not use.



## -syntax

````
SIZE_T ReadFromHardware(
  [in]           WDF_DEVICE_HWACCESS_TARGET_TYPE Type,
  [in]           WDF_DEVICE_HWACCESS_TARGET_SIZE Size,
  [in]           VOID                            *Address,
  [out]          VOID                            *Buffer,
  [in, optional] ULONG                           Count
);
````


## -parameters

### -param Type [in]


### -param Size [in]


### -param Address [in]


### -param Buffer [out]


### -param Count [in, optional]


## -remarks


## -see-also
<dl>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdfdevice3.md">IWDFDevice3</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IWDFDevice3::ReadFromHardware method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

