---
UID: NS:hidsdi._HIDD_ATTRIBUTES
title: _HIDD_ATTRIBUTES
author: windows-driver-content
description: The HIDD_ATTRIBUTES structure contains vendor information about a HIDClass device.
old-location: hid\hidd_attributes.htm
old-project: hid
ms.assetid: 31bfa863-459f-4fb2-af41-2d40d0396dd7
ms.author: windowsdriverdev
ms.date: 12/21/2017
ms.keywords: _HIDD_ATTRIBUTES, *PHIDD_ATTRIBUTES, HIDD_ATTRIBUTES
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: hidsdi.h
req.include-header: Hidsdi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: HIDD_ATTRIBUTES
req.alt-loc: hidsdi.h
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
req.typenames: *PHIDD_ATTRIBUTES, HIDD_ATTRIBUTES
---

# _HIDD_ATTRIBUTES structure



## -description
The HIDD_ATTRIBUTES structure contains vendor information about a HIDClass device.



## -syntax

````
typedef struct _HIDD_ATTRIBUTES {
  ULONG  Size;
  USHORT VendorID;
  USHORT ProductID;
  USHORT VersionNumber;
} HIDD_ATTRIBUTES, *PHIDD_ATTRIBUTES;
````


## -struct-fields

### -field Size

Specifies the size, in bytes, of a HIDD_ATTRIBUTES structure.


### -field VendorID

Specifies a HID device's vendor ID.


### -field ProductID

Specifies a HID device's product ID.


### -field VersionNumber

Specifies the manufacturer's revision number for a HIDClass device.


## -remarks
A caller of <a href="..\hidsdi\nf-hidsdi-hidd_getattributes.md">HidD_GetAttributes</a>, uses this structure to obtain a device's vendor information.

Before using a HIDD_ATTRIBUTES structure with <a href="https://msdn.microsoft.com/library/windows/hardware/ff538865">HIDClass support routines</a>, the caller must set the <b>Size</b> member.


## -see-also
<dl>
<dt>
<a href="..\hidsdi\nf-hidsdi-hidd_getattributes.md">HidD_GetAttributes</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [hid\hid]:%20HIDD_ATTRIBUTES structure%20 RELEASE:%20(12/21/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

