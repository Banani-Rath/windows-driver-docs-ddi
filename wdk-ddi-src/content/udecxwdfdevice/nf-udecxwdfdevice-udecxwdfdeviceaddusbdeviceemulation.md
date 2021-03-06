---
UID: NF:udecxwdfdevice.UdecxWdfDeviceAddUsbDeviceEmulation
title: UdecxWdfDeviceAddUsbDeviceEmulation function
author: windows-driver-content
description: Initializes a framework device object to support operations related to a host controller and a virtual USB device attached to the controller.
old-location: buses\udecxwdfdeviceaddusbdeviceemulation.htm
old-project: usbref
ms.assetid: EE7644A9-AA57-4C53-9FA5-F844F2BFB0D7
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: UdecxWdfDeviceAddUsbDeviceEmulation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: udecxwdfdevice.h
req.include-header: Udecx.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 1.15
req.umdf-ver: 
req.alt-api: UdecxWdfDeviceAddUsbDeviceEmulation
req.alt-loc: Udecxstub.lib,Udecxstub.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Udecxstub.lib
req.dll: 
req.irql: PASSIVE_LEVEL
req.typenames: UDECX_WDF_DEVICE_RESET_ACTION, *PUDECX_WDF_DEVICE_RESET_ACTION
req.product: Windows 10 or later.
---

# UdecxWdfDeviceAddUsbDeviceEmulation function



## -description
Initializes a framework device object to support operations related to a host controller and a virtual USB device attached to the controller. 



## -syntax

````
FORCEINLINE NTSTATUS UdecxWdfDeviceAddUsbDeviceEmulation(
  _In_ WDFDEVICE                Device,
  _In_ PUDECX_WDF_DEVICE_CONFIG Config
);
````


## -parameters

### -param Device [in]

A handle to the framework device object that the client driver retrieved in the previous call to <a href="..\wdfdevice\nf-wdfdevice-wdfdevicecreate.md">WdfDeviceCreate</a>.


### -param Config [in]

 A pointer to a <a href="..\udecxwdfdevice\ns-udecxwdfdevice-_udecx_wdf_device_config.md">UDECX_WDF_DEVICE_CONFIG</a> structure that the client driver initialized by calling <a href="..\udecxwdfdevice\nf-udecxwdfdevice-udecx_wdf_device_config_init.md">UDECX_WDF_DEVICE_CONFIG_INIT</a>.


## -returns
The method returns STATUS_SUCCESS if the operation succeeds. Otherwise, this method might return an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code. 


## -remarks
The UDE client driver for the emulated host controller and the USB device must call this method after the <a href="..\wdfdevice\nf-wdfdevice-wdfdevicecreate.md">WdfDeviceCreate</a> call. 

During this call, the client driver-supplied event callback implementations are also registered. Supply function  pointers to those functions by call setting appropriate members of <a href="..\udecxwdfdevice\ns-udecxwdfdevice-_udecx_wdf_device_config.md">UDECX_WDF_DEVICE_CONFIG</a>. 

The method makes the framework device object capable of performing operations related to a controller and its root hub, such as handling various queues required to process IOCTL requests sent to the attached USB device. 


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/mt595932">Architecture: USB Device Emulation (UDE)</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/mt595939">Write a UDE client driver</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20UdecxWdfDeviceAddUsbDeviceEmulation function%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

