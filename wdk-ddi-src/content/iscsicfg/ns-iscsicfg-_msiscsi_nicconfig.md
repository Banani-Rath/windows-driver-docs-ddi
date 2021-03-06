---
UID: NS:iscsicfg._MSiSCSI_NICConfig
title: _MSiSCSI_NICConfig
author: windows-driver-content
description: The MSiSCSI_NICConfig structure describes the configuration of a network interface card (NIC) port.
old-location: storage\msiscsi_nicconfig.htm
old-project: storage
ms.assetid: ee40ea1f-fe9b-4126-b5b1-83f60cf51909
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: _MSiSCSI_NICConfig, *PMSiSCSI_NICConfig, MSiSCSI_NICConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iscsicfg.h
req.include-header: Iscsicfg.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: MSiSCSI_NICConfig
req.alt-loc: iscsicfg.h
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
req.typenames: *PMSiSCSI_NICConfig, MSiSCSI_NICConfig
---

# _MSiSCSI_NICConfig structure



## -description
The MSiSCSI_NICConfig structure describes the configuration of a network interface card (NIC) port.



## -syntax

````
typedef struct _MSiSCSI_NICConfig {
  ULONG LinkSpeed;
  ULONG MaxLinkSpeed;
  ULONG LinkState;
  ULONG MaxFrameSize;
  UCHAR MacAddress[6];
} MSiSCSI_NICConfig, *PMSiSCSI_NICConfig;
````


## -struct-fields

### -field LinkSpeed

The speed of the network link, in megabits per second.


### -field MaxLinkSpeed

The maximum speed of the network link, in megabits per second (Mbps).


### -field LinkState

A <a href="..\iscsicfg\ne-iscsicfg-piscsi_nic_linkstate.md">ISCSI_NIC_LINKSTATE</a> enumeration value that indicates whether the port is connected to the network or not.


### -field MaxFrameSize

The maximum frame size, in bytes.


### -field MacAddress

The Ethernet MAC address of the port.


## -remarks
The WMI tool suite automatically generates a declaration of the MSiSCSI_NICConfig structure when it compiles the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563083">MSiSCSI_NICConfig WMI Class</a> in <i>Config.mof</i>.

Initiators are <i>not </i>required to implement the MSiSCSI_NICConfig class. 

Initiators that implement the MSiSCSI_NICConfig class should create one instance of the class for each network port on the adapter. 

Initiators should register each instance of the MSiSCSI_NICConfig class by using the name of the physical device object (PDO) for the corresponding network port. It is optional that you implement this class.


## -see-also
<dl>
<dt>
<a href="..\iscsicfg\ne-iscsicfg-piscsi_nic_linkstate.md">ISCSI_NIC_LINKSTATE</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563083">MSiSCSI_NICConfig WMI Class</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20MSiSCSI_NICConfig structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

