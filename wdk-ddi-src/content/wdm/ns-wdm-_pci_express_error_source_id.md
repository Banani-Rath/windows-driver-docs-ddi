---
UID: NS:wdm._PCI_EXPRESS_ERROR_SOURCE_ID
title: _PCI_EXPRESS_ERROR_SOURCE_ID
author: windows-driver-content
description: The PCI_EXPRESS_ERROR_SOURCE_ID structure describes the identifiers of the first correctable error and the first uncorrectable error that are reported in the PCI Express (PCIe) root error status register.
old-location: pci\pci_express_error_source_id.htm
old-project: PCI
ms.assetid: 53efddbc-0e65-487c-b406-c7d093ca5667
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: _PCI_EXPRESS_ERROR_SOURCE_ID, PCI_EXPRESS_ERROR_SOURCE_ID, *PPCI_EXPRESS_ERROR_SOURCE_ID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wdm.h
req.include-header: Ntddk.h, Wdm.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: PCI_EXPRESS_ERROR_SOURCE_ID
req.alt-loc: wdm.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL (see Remarks section)
req.typenames: PCI_EXPRESS_ERROR_SOURCE_ID, *PPCI_EXPRESS_ERROR_SOURCE_ID
req.product: Windows 10 or later.
---

# _PCI_EXPRESS_ERROR_SOURCE_ID structure



## -description
The PCI_EXPRESS_ERROR_SOURCE_ID structure describes the identifiers of the first correctable error and the first uncorrectable error that are reported in the PCI Express (PCIe) root error status register.



## -syntax

````
typedef union _PCI_EXPRESS_ERROR_SOURCE_ID {
  struct {
    USHORT CorrectableSourceIdFun  :3;
    USHORT CorrectableSourceIdDev  :5;
    USHORT CorrectableSourceIdBus  :8;
    USHORT UncorrectableSourceIdFun  :3;
    USHORT UncorrectableSourceIdDev  :5;
    USHORT UncorrectableSourceIdBus  :8;
  };
  ULONG  AsULONG;
} PCI_EXPRESS_ERROR_SOURCE_ID, *PPCI_EXPRESS_ERROR_SOURCE_ID;
````


## -struct-fields

### -field CorrectableSourceIdFun

The function number of the requester that reported the first correctable error.


### -field CorrectableSourceIdDev

The device number of the requester that reported the first correctable error.


### -field CorrectableSourceIdBus

The bus number of the requester that reported the first correctable error.


### -field UncorrectableSourceIdFun

The function number of the requester that reported the first uncorrectable error.


### -field UncorrectableSourceIdDev

The device number of the requester that reported the first uncorrectable error.


### -field UncorrectableSourceIdBus

The bus number of the requester that reported the first uncorrectable error.


### -field AsULONG

A ULONG representation of the contents of the PCI_EXPRESS_ERROR_SOURCE_ID structure.


## -remarks
The PCI_EXPRESS_ERROR_SOURCE_ID structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_ERROR_SOURCE_ID structure is contained in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a> structure.


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [PCI\buses]:%20PCI_EXPRESS_ERROR_SOURCE_ID union%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

