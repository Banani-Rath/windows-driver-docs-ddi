---
UID: NF:fltkernel.FltGetRequestorProcess
title: FltGetRequestorProcess function
author: windows-driver-content
description: The FltGetRequestorProcess routine returns a process pointer for the thread that requested a given I/O operation.
old-location: ifsk\fltgetrequestorprocess.htm
old-project: ifsk
ms.assetid: be734d14-64ee-47f0-8df9-4c4b8830448d
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: FltGetRequestorProcess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fltkernel.h
req.include-header: Fltkernel.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: FltGetRequestorProcess
req.alt-loc: fltmgr.sys
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FltMgr.lib
req.dll: Fltmgr.sys
req.irql: <= DISPATCH_LEVEL
req.typenames: EXpsFontRestriction
---

# FltGetRequestorProcess function



## -description
The <b>FltGetRequestorProcess</b> routine returns a process pointer for the thread that requested a given I/O operation. 



## -syntax

````
PEPROCESS FltGetRequestorProcess(
  _In_ PFLT_CALLBACK_DATA CallbackData
);
````


## -parameters

### -param CallbackData [in]

Pointer to the callback data structure (<a href="..\fltkernel\ns-fltkernel-_flt_callback_data.md">FLT_CALLBACK_DATA</a>) for the I/O operation. 


## -returns
<b>FltGetRequestorProcess</b> returns a process pointer for the thread that requested the I/O operation. If the operation is not associated with any thread, <b>FltGetRequestorProcess</b> returns <b>NULL</b>. 


## -remarks
<b>FltGetRequestorProcess</b> returns a pointer to the process that the requesting thread is currently attached to. This process may or may not be the same process that created the thread. 


## -see-also
<dl>
<dt>
<a href="..\fltkernel\ns-fltkernel-_flt_callback_data.md">FLT_CALLBACK_DATA</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltgetrequestorprocessid.md">FltGetRequestorProcessId</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FltGetRequestorProcess routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

