---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvDeleteItem
title: IWiaMiniDrv::drvDeleteItem method
author: windows-driver-content
description: The IWiaMiniDrv::drvDeleteItem method deletes the current driver item.
old-location: image\iwiaminidrv_drvdeleteitem.htm
old-project: image
ms.assetid: 616a0edd-d769-411d-bc94-57ba18a00c4d
ms.author: windowsdriverdev
ms.date: 1/17/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv::drvDeleteItem, drvDeleteItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IWiaMiniDrv.drvDeleteItem
req.alt-loc: wiamindr_lh.h
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
req.typenames: *PSCANWINDOW, SCANWINDOW
req.product: Windows 10 or later.
---

# IWiaMiniDrv::drvDeleteItem method



## -description
The <b>IWiaMiniDrv::drvDeleteItem</b> method deletes the current driver item.



## -syntax

````
HRESULT drvDeleteItem(
  [in]  BYTE *pWiasContext,
  [in]  LONG lFlags,
  [out] LONG *plDevErrVal
);
````


## -parameters

### -param pWiasContext [in]

Pointer to a WIA item context.


### -param lFlags [in]

Is currently unused. 


### -param plDevErrVal [out]

Points to a memory location that will receive a status code for this method. If this method returns S_OK, the value stored will be zero. Otherwise, a minidriver-specific error code will be stored at the location pointed to by this parameter.


## -returns
On success, the method should return S_OK and clear the device error value pointed to by <i>plDevErrVal</i>. If the method fails, it should return a standard COM error code and place a minidriver-specific error code value in the memory pointed to by <i>plDevErrVal</i>. The value pointed to by <i>plDevErrVal</i> can be converted to a string by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>.


## -remarks
In order to delete a driver item, the WIA service will call the minidriver method <b>IWiaMiniDrv::drvDeleteItem</b>. In this method, the minidriver will attempt to delete the item pointed to by the WIA service context parameter <i>pWiasContext</i>. If the item is successfully deleted, the method returns S_OK and sets the device error value parameter <i>plDevErrVal</i> to zero. If a device error occurs, the method returns E_FAIL and a device-specific error value in the device error value parameter <i>plDevErrVal</i>.

Before the WIA service calls this method, it verifies the following:

The item is not the root item.

If the item is a folder, it does not have any children.

The item's access rights allow deletion.

Since the WIA service verifies these conditions, it is not necessary for the minidriver to also verify them.


## -see-also
<dl>
<dt>
<a href="..\wiamindr_lh\nn-wiamindr_lh-iwiaminidrv.md">IWiaMiniDrv</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543982">IWiaMiniDrv::drvGetDeviceErrorStr</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [image\image]:%20IWiaMiniDrv::drvDeleteItem method%20 RELEASE:%20(1/17/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

