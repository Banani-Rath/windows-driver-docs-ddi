---
UID: NS:hbapiwmi._MS_SMHBA_SCSIENTRY
title: _MS_SMHBA_SCSIENTRY
author: windows-driver-content
description: The MS_SMHBA_SCSIENTRY structure is used to report target LUN mapping information.
old-location: storage\ms_smhba_scsientry.htm
old-project: storage
ms.assetid: 38779458-a561-4048-86d8-905e4e50095f
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: _MS_SMHBA_SCSIENTRY, MS_SMHBA_SCSIENTRY, *PMS_SMHBA_SCSIENTRY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: hbapiwmi.h
req.include-header: Hbapiwmi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: MS_SMHBA_SCSIENTRY
req.alt-loc: hbapiwmi.h
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
req.typenames: MS_SMHBA_SCSIENTRY, *PMS_SMHBA_SCSIENTRY
---

# _MS_SMHBA_SCSIENTRY structure



## -description
The MS_SMHBA_SCSIENTRY structure is used to report target LUN mapping information.



## -syntax

````
typedef struct _MS_SMHBA_SCSIENTRY {
  MS_SMHBA_PORTLUN PortLun;
  UCHAR            LUID[256];
  HBAScsiID        ScsiId;
} MS_SMHBA_SCSIENTRY, *PMS_SMHBA_SCSIENTRY;
````


## -struct-fields

### -field PortLun

An array of MS_SMHBA_PORTLUN entries.


### -field LUID

The logical unit descriptor for the device that the operating system derives from SCSI inquiry data.


### -field ScsiId

A structure of type HBAScsiID that contains information that uniquely identifies a logical unit to the operating system.


## -remarks
