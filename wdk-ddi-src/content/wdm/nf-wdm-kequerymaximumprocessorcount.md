---
UID: NF:wdm.KeQueryMaximumProcessorCount
title: KeQueryMaximumProcessorCount function
author: windows-driver-content
description: The KeQueryMaximumProcessorCount routine returns the maximum number of processors.
old-location: kernel\kequerymaximumprocessorcount.htm
old-project: kernel
ms.assetid: bab2c478-4e46-40d9-a4b6-6f322b18ab0a
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: KeQueryMaximumProcessorCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: KeQueryMaximumProcessorCount
req.alt-loc: NtosKrnl.exe
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: Any level
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# KeQueryMaximumProcessorCount function



## -description
The <b>KeQueryMaximumProcessorCount</b> routine returns the maximum number of processors.



## -syntax

````
ULONG KeQueryMaximumProcessorCount(void);
````


## -parameters


## -returns
<b>KeQueryMaximumProcessorCount</b> returns the maximum number of processors as a ULONG value.

<b>KeQueryMaximumProcessorCount</b> returns the maximum number of processors as a ULONG value.

<b>KeQueryMaximumProcessorCount</b> returns the maximum number of processors as a ULONG value.


## -remarks
The value returned by the <b>KeQueryMaximumProcessorCount</b> routine does not change at runtime.

If your code uses an array of buffers, one buffer for each processor, you must decide whether to have a statically sized array based on <b>KeQueryMaximumProcessorCount</b> or a dynamically sized array based on <a href="..\wdm\nf-wdm-kequeryactiveprocessorcount.md">KeQueryActiveProcessorCount</a>.

To optimize based on the number of processors, you need a resizable structure for Windows Server 2008. In this case, use <b>KeQueryActiveProcessorCount</b>.

If you are not optimizing and if the data structures that result from using maximum processor count are relatively small, a resizable structure is not necessary. In this case, use <b>KeQueryMaximumProcessorCount</b> to determine size for a static array.

Windows 7 and later versions of Windows support processor groups. Drivers that are designed to handle information about processor groups should use the <a href="..\ntddk\nf-ntddk-kequerymaximumprocessorcountex.md">KeQueryMaximumProcessorCountEx</a> routine, which specifies a processor group, instead of <b>KeQueryMaximumProcessorCount</b>, which does not. However, the implementation of <b>KeQueryMaximumProcessorCount</b> in Windows 7 and later versions of Windows provides compatibility for drivers that were written for earlier versions of Windows, which do not support processor groups. In this implementation, <b>KeQueryMaximumProcessorCount</b> returns the maximum number of logical processors that can be in group 0.


## -see-also
<dl>
<dt>
<a href="..\wdm\nf-wdm-kequeryactiveprocessorcount.md">KeQueryActiveProcessorCount</a>
</dt>
<dt>
<a href="..\ntddk\nf-ntddk-kequerymaximumprocessorcountex.md">KeQueryMaximumProcessorCountEx</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20KeQueryMaximumProcessorCount routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

