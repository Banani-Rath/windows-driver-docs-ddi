---
UID: NF:winsplp.RouterFreeBidiMem
title: RouterFreeBidiMem function
author: windows-driver-content
description: RouterFreeBidiMem frees a block of memory that was previously allocated by RouterAllocBidiMem.
old-location: print\routerfreebidimem.htm
old-project: print
ms.assetid: 946b1630-844a-43ac-8c26-fdfa2ee7866a
ms.author: windowsdriverdev
ms.date: 1/8/2018
ms.keywords: RouterFreeBidiMem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsplp.h
req.include-header: Winsplp.h
req.target-type: Desktop
req.target-min-winverclnt: This function is available in Windows XP and later operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: RouterFreeBidiMem
req.alt-loc: Spoolss.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Spoolss.lib
req.dll: Spoolss.dll
req.irql: 
req.typenames: NOTIFICATION_CONFIG_FLAGS
req.product: Windows 10 or later.
---

# RouterFreeBidiMem function



## -description
<code>RouterFreeBidiMem</code> frees a block of memory that was previously allocated by <a href="..\winsplp\nf-winsplp-routerallocbidimem.md">RouterAllocBidiMem</a>.



## -syntax

````
VOID RouterFreeBidiMem(
  _In_ PVOID pMemPointer
);
````


## -parameters

### -param pMemPointer [in]

Pointer to the memory to be freed.


## -returns
None


## -remarks


## -see-also
<dl>
<dt>
<a href="..\winsplp\nf-winsplp-routerallocbidimem.md">RouterAllocBidiMem</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20RouterFreeBidiMem function%20 RELEASE:%20(1/8/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

