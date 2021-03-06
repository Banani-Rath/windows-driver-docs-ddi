---
UID: NF:wdm.READ_PORT_ULONG
title: READ_PORT_ULONG function
author: windows-driver-content
description: The READ_PORT_ULONG routine reads a ULONG value from the specified port address.
old-location: kernel\read_port_ulong.htm
old-project: kernel
ms.assetid: 8a2f4429-b805-4a36-afdf-8b9c9a886951
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: READ_PORT_ULONG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: READ_PORT_ULONG
req.alt-loc: Hal.lib,Hal.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Hal.lib
req.dll: 
req.irql: Any level (see Remarks section)
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# READ_PORT_ULONG function



## -description
The <b>READ_PORT_ULONG</b> routine reads a ULONG value from the specified port address.



## -syntax

````
ULONG READ_PORT_ULONG(
  _In_ PULONG Port
);
````


## -parameters

### -param Port [in]

Specifies the port address, which must be a mapped range in I/O space. 


## -returns
<b>READ_PORT_ULONG</b> returns the ULONG value that is read from the specified port address.


## -remarks
Callers of <b>READ_PORT_ULONG</b> can be running at any IRQL, assuming the <i>Port</i> is resident, mapped device memory.</p>