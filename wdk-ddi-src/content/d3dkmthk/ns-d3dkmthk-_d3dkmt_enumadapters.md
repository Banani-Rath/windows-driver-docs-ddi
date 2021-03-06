---
UID: NS:d3dkmthk._D3DKMT_ENUMADAPTERS
title: _D3DKMT_ENUMADAPTERS
author: windows-driver-content
description: Supplies information for enumerating all graphics adapters on the system.
old-location: display\d3dkmt_enumadapters.htm
old-project: display
ms.assetid: a05252bc-6bc4-4cef-aa42-e2c03556847a
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: _D3DKMT_ENUMADAPTERS, D3DKMT_ENUMADAPTERS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: D3DKMT_ENUMADAPTERS
req.alt-loc: D3dkmthk.h
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
req.typenames: D3DKMT_ENUMADAPTERS
---

# _D3DKMT_ENUMADAPTERS structure



## -description
Supplies information for  enumerating all graphics adapters on the system.



## -syntax

````
typedef struct _D3DKMT_ENUMADAPTERS {
  ULONG              NumAdapters;
  D3DKMT_ADAPTERINFO Adapters[MAX_ENUM_ADAPTERS];
} D3DKMT_ENUMADAPTERS;
````


## -struct-fields

### -field NumAdapters

[in] The number of graphics adapters.


### -field Adapters

An array of <a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_adapterinfo.md">D3DKMT_ADAPTERINFO</a> structures that supply configuration information for each adapter. The maximum number of adapters that can be enumerated is 16.


## -remarks


## -see-also
<dl>
<dt>
<a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_adapterinfo.md">D3DKMT_ADAPTERINFO</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DKMT_ENUMADAPTERS structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

