---
UID: NS:avc._AVC_PIN_COUNT
title: _AVC_PIN_COUNT
author: windows-driver-content
description: The AVC_PIN_COUNT structure specifies the number of pins on an AV/C subunit device.
old-location: stream\avc_pin_count.htm
old-project: stream
ms.assetid: e43557ed-3394-47df-9581-fc3f0c314529
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: _AVC_PIN_COUNT, *PAVC_PIN_COUNT, AVC_PIN_COUNT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: avc.h
req.include-header: Avc.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: AVC_PIN_COUNT
req.alt-loc: avc.h
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
req.typenames: *PAVC_PIN_COUNT, AVC_PIN_COUNT
---

# _AVC_PIN_COUNT structure



## -description
The AVC_PIN_COUNT structure specifies the number of pins on an AV/C subunit device.



## -syntax

````
typedef struct _AVC_PIN_COUNT {
  ULONG PinCount;
} AVC_PIN_COUNT, *PAVC_PIN_COUNT;
````


## -struct-fields

### -field PinCount

This value is filled in by <i>avc.sys</i> on return from the <b>AVC_FUNCTION_GET_PIN_COUNT</b> function.


## -remarks
This structure is used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff554158">AVC_FUNCTION_GET_PIN_COUNT</a> function code.

This structure is used only as a member inside the AVC_MULTIFUNC_IRB structure. It is not used by itself.

See <a href="https://msdn.microsoft.com/3b4ec139-ff01-40bd-8e29-92f554180585">How to Use Avc.sys</a> For information about building and sending an AV/C command.


## -see-also
<dl>
<dt>
<a href="..\avc\ns-avc-_avc_multifunc_irb.md">AVC_MULTIFUNC_IRB</a>
</dt>
<dt>
<a href="..\avc\ne-avc-_tagavc_function.md">AVC_FUNCTION</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff554158">AVC_FUNCTION_GET_PIN_COUNT</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20AVC_PIN_COUNT structure%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

