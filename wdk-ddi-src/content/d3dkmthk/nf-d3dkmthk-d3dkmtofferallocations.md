---
UID: NF:d3dkmthk.D3DKMTOfferAllocations
title: D3DKMTOfferAllocations function
author: windows-driver-content
description: Offers video memory allocations for reuse.
old-location: display\d3dkmtofferallocations.htm
old-project: display
ms.assetid: 3cc84381-fa1e-4c6c-bb5b-459a93676cfd
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: D3DKMTOfferAllocations
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Universal
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: D3DKMTOfferAllocations
req.alt-loc: Gdi32.dll,API-MS-Win-DX-D3DKmt-l1-1-0.dll,API-MS-Win-DX-D3DKmt-l1-1-1.dll,API-MS-Win-DX-D3DKMT-L1-1-2.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.typenames: D3DKMT_DRIVERVERSION
---

# D3DKMTOfferAllocations function



## -description
Offers video memory allocations for reuse.



## -syntax

````
EXTERN_C _Check_return_ NTSTATUS APIENTRY D3DKMTOfferAllocations(
  _In_ const D3DKMT_OFFERALLOCATIONS *pData
);
````


## -parameters

### -param pData [in]

A pointer to a <a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_offerallocations.md">D3DKMT_OFFERALLOCATIONS</a> structure that defines memory allocations that the driver offers for reuse.


## -returns
Returns one of the following values:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The allocations were successfully offered.
<dl>
<dt><b>STATUS_DEVICE_REMOVED</b></dt>
</dl>The graphics adapter was stopped or the display device was reset.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>Parameters were validated and determined to be incorrect.

 


## -remarks


## -see-also
<dl>
<dt>
<a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_offerallocations.md">D3DKMT_OFFERALLOCATIONS</a>
</dt>
<dt>
<a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtreclaimallocations.md">D3DKMTReclaimAllocations</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DKMTOfferAllocations function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

