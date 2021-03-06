---
UID: NS:ksmedia.KS_AM_SimpleRateChange
title: KS_AM_SimpleRateChange
author: windows-driver-content
description: The KS_AM_SimpleRateChange structure is used to describe a simple rate change (fast-forward or rewind) for an MPEG2 stream.
old-location: stream\ks_am_simpleratechange.htm
old-project: stream
ms.assetid: d797b377-6c27-41f9-932d-264d0e8b5dd0
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: KS_AM_SimpleRateChange, *PKS_AM_SimpleRateChange, KS_AM_SimpleRateChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: KS_AM_SimpleRateChange
req.alt-loc: ksmedia.h
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
req.typenames: *PKS_AM_SimpleRateChange, KS_AM_SimpleRateChange
---

# KS_AM_SimpleRateChange structure



## -description
The KS_AM_SimpleRateChange structure is used to describe a simple rate change (fast-forward or rewind) for an MPEG2 stream.



## -syntax

````
typedef struct {
  REFERENCE_TIME StartTime;
  LONG           Rate;
} KS_AM_SimpleRateChange, *PKS_AM_SimpleRateChange;
````


## -struct-fields

### -field StartTime

Indicates the stream time at which to start this rate.


### -field Rate

Specifies the new rate. This value is multiplied by 10000 (decimal).


## -remarks


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff567288">KS_AM_RATE_SimpleRateChange</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KS_AM_SimpleRateChange structure%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

