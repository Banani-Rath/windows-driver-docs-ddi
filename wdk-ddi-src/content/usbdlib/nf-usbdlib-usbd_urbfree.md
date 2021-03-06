---
UID: NF:usbdlib.USBD_UrbFree
title: USBD_UrbFree function
author: windows-driver-content
description: The USBD_UrbFree routine releases the URB that is allocated by USBD_UrbAllocate, USBD_IsochUrbAllocate, USBD_SelectConfigUrbAllocateAndBuild, or USBD_SelectInterfaceUrbAllocateAndBuild.
old-location: buses\usbd_urbfree.htm
old-project: usbref
ms.assetid: DD80BAA0-EC01-4231-827A-962580D1E201
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: USBD_UrbFree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: usbdlib.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Requires WDK for Windows 8. Targets Windows Vista and later versions of the Windows operating system.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: USBD_UrbFree
req.alt-loc: Usbdex.lib,Usbdex.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Usbdex.lib
req.dll: 
req.irql: <=DISPATCH_LEVEL
req.typenames: USBCAMD_DEVICE_DATA2, *PUSBCAMD_DEVICE_DATA2
req.product: Windows 10 or later.
---

# USBD_UrbFree function



## -description
The <b>USBD_UrbFree</b> routine releases the <a href="..\usb\ns-usb-_urb.md">URB</a> that is allocated by <a href="..\usbdlib\nf-usbdlib-usbd_urballocate.md">USBD_UrbAllocate</a>, <a href="..\usbdlib\nf-usbdlib-usbd_isochurballocate.md">USBD_IsochUrbAllocate</a>, <a href="..\usbdlib\nf-usbdlib-usbd_selectconfigurballocateandbuild.md">USBD_SelectConfigUrbAllocateAndBuild</a>, or 
    <a href="..\usbdlib\nf-usbdlib-usbd_selectinterfaceurballocateandbuild.md">USBD_SelectInterfaceUrbAllocateAndBuild</a>.



## -syntax

````
void USBD_UrbFree(
  _In_ USBD_HANDLE USBDHandle,
  _In_ PURB        Urb
);
````


## -parameters

### -param USBDHandle [in]

USBD handle that is retrieved by the client driver in a previous call to  the <a href="..\usbdlib\nf-usbdlib-usbd_createhandle.md">USBD_CreateHandle</a> routine.


### -param Urb [in]

Pointer to the <a href="..\usb\ns-usb-_urb.md">URB</a> structure to be released.


## -returns
This routine does not return a value.


## -remarks
You must call <b>USBD_UrbFree</b> to release the URB allocated by <a href="..\usbdlib\nf-usbdlib-usbd_urballocate.md">USBD_UrbAllocate</a> after the request is complete. 

Failure to call <b>USBD_UrbFree</b> can cause a memory leak. 

For a code example, see <a href="..\usbdlib\nf-usbdlib-usbd_urballocate.md">USBD_UrbAllocate</a>.


## -see-also
<dl>
<dt>
<a href="..\usbdlib\nf-usbdlib-usbd_urballocate.md">USBD_UrbAllocate</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450844">Allocating and Building URBs</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20USBD_UrbFree routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

