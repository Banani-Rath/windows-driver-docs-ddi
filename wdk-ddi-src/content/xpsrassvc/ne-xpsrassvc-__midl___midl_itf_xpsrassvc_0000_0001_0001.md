---
UID: NE:xpsrassvc.__MIDL___MIDL_itf_xpsrassvc_0000_0001_0001
title: __MIDL___MIDL_itf_xpsrassvc_0000_0001_0001
author: windows-driver-content
description: The XPSRAS_RENDERING_MODE enumeration specifies the rendering mode to be used by an XPS rasterizer.
old-location: print\xpsras_rendering_mode_enumeration.htm
old-project: print
ms.assetid: 8b0b2bde-6ada-4a73-9737-7150605b79c8
ms.author: windowsdriverdev
ms.date: 1/8/2018
ms.keywords: __MIDL___MIDL_itf_xpsrassvc_0000_0001_0001, XPSRAS_RENDERING_MODE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: xpsrassvc.h
req.include-header: Xpsrassvc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: XPSRAS_RENDERING_MODE
req.alt-loc: xpsrassvc.h
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
req.typenames: XPSRAS_RENDERING_MODE
req.product: Windows 10 or later.
---

# __MIDL___MIDL_itf_xpsrassvc_0000_0001_0001 enumeration



## -description
The XPSRAS_RENDERING_MODE enumeration specifies the rendering mode to be used by an XPS rasterizer.



## -syntax

````
typedef enum  { 
  XPSRAS_RENDERING_MODE_ANTIALIASED  = 0,
  XPSRAS_RENDERING_MODE_ALIASED      = 1
} XPSRAS_RENDERING_MODE;
````


## -enum-fields

### -field XPSRAS_RENDERING_MODE_ANTIALIASED

Use antialiasing to rasterize the specified graphics elements.


### -field XPSRAS_RENDERING_MODE_ALIASED

Do not use antialiasing to rasterize the specified graphics elements.


## -remarks
The values defined in this enumeration are used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556350">IXpsRasterizationFactory::CreateRasterizer</a> method.

For more information about rasterizing XPS documents, see <a href="https://msdn.microsoft.com/a6a3746a-3638-464b-bca0-60003f37af76">Using the XPS Rasterization Service</a>.


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556350">IXpsRasterizationFactory::CreateRasterizer</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20XPSRAS_RENDERING_MODE enumeration%20 RELEASE:%20(1/8/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

