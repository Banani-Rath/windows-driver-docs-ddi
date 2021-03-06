---
UID: NF:fltkernel.FltRetainSwappedBufferMdlAddress
title: FltRetainSwappedBufferMdlAddress function
author: windows-driver-content
description: FltRetainSwappedBufferMdlAddress prevents the Filter Manager from freeing the memory descriptor list (MDL) for a buffer that was swapped in by a minifilter driver.
old-location: ifsk\fltretainswappedbuffermdladdress.htm
old-project: ifsk
ms.assetid: 80498410-9617-414d-997c-0d55f891ba3c
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: FltRetainSwappedBufferMdlAddress
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
req.alt-api: FltRetainSwappedBufferMdlAddress
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
req.irql: Any level
req.typenames: EXpsFontRestriction
---

# FltRetainSwappedBufferMdlAddress function



## -description
<b>FltRetainSwappedBufferMdlAddress</b> prevents the Filter Manager from freeing the memory descriptor list (MDL) for a buffer that was swapped in by a minifilter driver. 



## -syntax

````
VOID FASTCALL FltRetainSwappedBufferMdlAddress(
  _In_ PFLT_CALLBACK_DATA CallbackData
);
````


## -parameters

### -param CallbackData [in]

Pointer to the callback data structure for the operation. 


## -returns
None 


## -remarks
When a minifilter driver swaps in a new buffer in a preoperation callback (<a href="..\fltkernel\nc-fltkernel-pflt_pre_operation_callback.md">PFLT_PRE_OPERATION_CALLBACK</a>) routine, the Filter Manager automatically frees the buffer's MDL when the corresponding postoperation (<a href="..\fltkernel\nc-fltkernel-pflt_post_operation_callback.md">PFLT_POST_OPERATION_CALLBACK</a>) callback routine returns. 

The minifilter driver can prevent the Filter Manager from freeing the MDL by calling <b>FltRetainSwappedBufferMdlAddress</b> from the postoperation callback routine. 

After calling <b>FltRetainSwappedBufferMdlAddress</b>, the caller is responsible for freeing the MDL by calling a routine such as <a href="..\wdm\nf-wdm-iofreemdl.md">IoFreeMdl</a>. 

<b>FltRetainSwappedBufferMdlAddress</b> can only be called from a postoperation callback routine. 


## -see-also
<dl>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltdecodeparameters.md">FltDecodeParameters</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltgetswappedbuffermdladdress.md">FltGetSwappedBufferMdlAddress</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iofreemdl.md">IoFreeMdl</a>
</dt>
<dt>
<a href="..\fltkernel\nc-fltkernel-pflt_post_operation_callback.md">PFLT_POST_OPERATION_CALLBACK</a>
</dt>
<dt>
<a href="..\fltkernel\nc-fltkernel-pflt_pre_operation_callback.md">PFLT_PRE_OPERATION_CALLBACK</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FltRetainSwappedBufferMdlAddress function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

