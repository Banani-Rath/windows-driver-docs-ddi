---
UID: NS:rilapitypes.RILUICCLOCK
title: RILUICCLOCK
author: windows-driver-content
description: This structure represents a RILUICCLOCK.
old-location: netvista\riluicclock.htm
old-project: netvista
ms.assetid: 634c2177-8e6f-4967-a555-928eb512fce3
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: RILUICCLOCK, *LPRILUICCLOCK, RILUICCLOCK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rilapitypes.h
req.include-header: Rilapitypes.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: RILUICCLOCK
req.alt-loc: rilapitypes.h
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
req.typenames: *LPRILUICCLOCK, RILUICCLOCK
req.product: Windows 10 or later.
---

# RILUICCLOCK structure



## -description

## -syntax

````
struct RILUICCLOCK {
  HUICCAPP hUiccApp;
  DWORD    dwKeyRef;
};
````


## -struct-fields

### -field hUiccApp

Specifies the UICC application context for this lock. In the case of PIN1 or UPIN, more than one application may make reference to the same key.


### -field dwKeyRef

The key for this lock of <a href="..\rilapitypes\ne-rilapitypes-riluicckeyref.md">RILUICCKEYREF</a> type. PIN1 keys are in the range 0x01..0x08 and may be shared by multiple applications. The Universal PIN is designated with key 0x11. PIN2 keys are in the range 0x81..0x88 and are local to each application (not shared). Two additional special values are defined: 0x00 represents a lock that is always verified (the “ALWays” access condition on the UICC) and 0xFF represents a lock that cannot be verified (the “NEVer” access condition).


## -remarks


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn946511">Cellular COM structures</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20RILUICCLOCK structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

