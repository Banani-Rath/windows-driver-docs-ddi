---
UID: NF:printerextension.IPrinterScriptableSequentialStream.Read
title: IPrinterScriptableSequentialStream::Read method
author: windows-driver-content
description: The Read method reads bytes from the stream and returns them as a JavaScript array.
old-location: print\iprinterscriptablesequentialstream_read.htm
old-project: print
ms.assetid: 1E13DF22-9C45-4475-8912-CC836EFC0A22
ms.author: windowsdriverdev
ms.date: 1/8/2018
ms.keywords: IPrinterScriptableSequentialStream, IPrinterScriptableSequentialStream::Read, Read
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: printerextension.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IPrinterScriptableSequentialStream.Read
req.alt-loc: printerextension.h
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
req.typenames: PrintSchemaSelectionType
req.product: Windows 10 or later.
---

# IPrinterScriptableSequentialStream::Read method



## -description
The Read method reads bytes from the stream and returns them as a JavaScript array.



## -syntax

````
HRESULT Read(
  [in]          LONG      cbRead,
  [out, retval] IDispatch **ppdispArray
);
````


## -parameters

### -param cbRead [in]

The number of bytes to read.


### -param ppdispArray [out, retval]

The returned array.


## -returns
This method returns an <b>HRESULT</b> value.


## -remarks


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/85DF7DCB-7AB1-4A46-AD70-6D47D9F98079">IPrinterScriptableSequentialStream</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPrinterScriptableSequentialStream::Read method%20 RELEASE:%20(1/8/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

