---
UID: NF:ks.KsAcquireDevice
title: KsAcquireDevice function
author: windows-driver-content
description: The KsAcquireDevice function gains synchronous access for Device by acquiring the device mutex.
old-location: stream\ksacquiredevice.htm
old-project: stream
ms.assetid: c486351a-b5a6-4a67-826d-6f66d04518b3
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: KsAcquireDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ks.h
req.include-header: Ks.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows XP and later operating systems and DirectX 8.0 and later DirectX versions.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: KsAcquireDevice
req.alt-loc: Ks.lib,Ks.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ks.lib
req.dll: 
req.irql: PASSIVE_LEVEL
req.typenames: 
---

# KsAcquireDevice function



## -description
The<b> KsAcquireDevice</b> function gains synchronous access for <i>Device</i> by acquiring the device mutex.



## -syntax

````
void KsAcquireDevice(
  _In_ PKSDEVICE Device
);
````


## -parameters

### -param Device [in]

An AVStream device for which synchronous control should be acquired.


## -returns
None


## -remarks
For more information, see <a href="https://msdn.microsoft.com/011edaaa-7449-41c3-8cfb-0d319901af8b">Mutexes in AVStream</a>.


## -see-also
<dl>
<dt>
<a href="..\ks\nf-ks-ksreleasedevice.md">KsReleaseDevice</a>
</dt>
<dt>
<a href="..\ks\ns-ks-_ksdevice.md">KSDEVICE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KsAcquireDevice function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

