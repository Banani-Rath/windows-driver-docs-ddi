---
UID: NI:scsi.IOCTL_SCSI_MINIPORT_DSM
title: IOCTL_SCSI_MINIPORT_DSM
author: windows-driver-content
description: A Data Set Management (DSM) notification is transferred to a miniport driver in a IOCTL_SCSI_MINIPORT_DSM control code request.
old-location: storage\ioctl_scsi_miniport_dsm.htm
old-project: storage
ms.assetid: CA91B623-F926-453D-A348-92655875D801
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: _SES_DOWNLOAD_MICROCODE_STATE, SES_DOWNLOAD_MICROCODE_STATE, *PSES_DOWNLOAD_MICROCODE_STATE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: scsi.h
req.include-header: Ntddscsi.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 8.1.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IOCTL_SCSI_MINIPORT_DSM
req.alt-loc: scsi.h
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
req.typenames: SES_DOWNLOAD_MICROCODE_STATE, *PSES_DOWNLOAD_MICROCODE_STATE
req.product: Windows 10 or later.
---

# IOCTL_SCSI_MINIPORT_DSM IOCTL



## -description
A Data Set Management (DSM) notification is transferred to a miniport driver in a 
     <b>IOCTL_SCSI_MINIPORT_DSM</b> control code request. The <b>IOCTL_SCSI_MINIPORT_DSM</b> request is a sub-IOCTL of <a href="..\ntddscsi\ni-ntddscsi-ioctl_scsi_miniport.md">IOCTL_SCSI_MINIPORT</a>. This IOCTL generated by StorPort in response to a DSM action, then sent  to the miniport as a <a href="..\srb\ns-srb-_storage_request_block.md">STORAGE_REQUEST_BLOCK</a> (SRB) with a function type of SRB_FUNCTION_IO_CONTROL. The input and output data is contained in the SRB data block. 



## -syntax

````
typedef struct _DSM_NOTIFICATION_REQUEST_BLOCK {
    ULONG   Version;
    ULONG   Size;
    ULONG   NotifyFLags;
    ULONG   DataSetProfile;
    ULONG   Reserved[3];
    ULONG   DataSetRangesCount;
    MP_DEVICE_DATA_SET_RANGE DataSetRanges[ANYSIZE_ARRAY];
} DSM_NOTIFICATION_REQUEST_BLOCK, *PDSM_NOTIFICATION_REQUEST_BLOCK;
````


## -ioctlparameters

### -input-buffer
The buffer specified in the <b>DataBuffer</b> member of the SRB must contain an <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure and a <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> structure.  


### -input-buffer-length
<b>DataTransferLength</b> indicates the size, in bytes, of the buffer, which must be at least <b>sizeof</b> (SRB_IO_CONTROL) + <b>sizeof</b>(DSM_NOTIFICATION_REQUEST_BLOCK), with additional storage for the <b>MP_DEVICE_DATA_SET_RANGE</b> structures included.


### -output-buffer
An updated <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure is returned to the data buffer in the SRB. The <b>SrbStatus</b> contains the result of the miniport's processing of the request.


### -output-buffer-length
The length of an <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure.


### -in-out-buffer

<text></text>

### -inout-buffer-length

<text></text>

### -status-block
I/O Status block
The resulting status of the function request is set in the <b>SrbStatus</b> member of <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a>. The following are the  DSM disk IOCTL status codes.

 


## -remarks
<b>DSM_NOTIFICATION_REQUEST_BLOCK</b>

A <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> structure immediately follows the <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure in the data buffer of the SRB.  <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> is defined in ntddscsi.h as the following.



The version of the structure. Set to MINIPORT_DSM_NOTIFICATION_VERSION.

The size of the structure. Set to <b>sizeof</b>(DSM_NOTIFICATION_REQUEST_BLOCK).

The notification flag. Indicates if the included LBA range is used as part of the file defined by the profile type.

The included LBA range is used as part of the file defined by the profile type.

The included LBA range is not used as part of the file defined by the profile type.

The profile type. Specifies the expected access pattern to the data set.

Unknown access pattern.

Page file access.

Hibernation file access.

Crash dump file access.

Reserved. Set to 0.

The count of <b>MP_DEVICE_DATA_SET_RANGE</b> structures in <b>DataSetRanges</b>.

An array of <b>MP_DEVICE_DATA_SET_RANGE</b> structures containing LBA ranges for the profile.

<b>MP_DEVICE_DATA_SET_RANGE</b>

The LBA ranges are included in the  in <b>DataSetRanges</b> member of <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> as an array of <b>MP_DEVICE_DATA_SET_RANGE</b> structures. <b>MP_DEVICE_DATA_SET_RANGE</b> is defined in ntddscsi.h as the following.

The starting offset, in bytes, of the data set range. The offset value must be block aligned.

The length, in bytes, of the data set range. The length value must be block aligned.

The <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> structure is located after the <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure in the <b>DataBuffer</b> of the SRB.

The <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure for this IOCTL contains IOCTL_MINIPORT_SIGNATURE_DSM_NOTIFICATION in its <b>Signature</b> member and <b>IOCTL_SCSI_MINIPORT_DSM</b> in the <b>ControlCode</b> member.


## -see-also
<dl>
<dt>
<a href="..\ntddscsi\ni-ntddscsi-ioctl_scsi_miniport.md">IOCTL_SCSI_MINIPORT</a>
</dt>
<dt>
<a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a>
</dt>
<dt>
<a href="..\srb\ns-srb-_storage_request_block.md">STORAGE_REQUEST_BLOCK</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20IOCTL_SCSI_MINIPORT_DSM control code%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

