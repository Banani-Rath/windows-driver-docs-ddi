---
UID: NF:dbgeng.IDebugSymbols3.AppendSourcePath
title: IDebugSymbols3::AppendSourcePath method
author: windows-driver-content
description: The AppendSourcePath method appends directories to the source path.
old-location: debugger\appendsourcepath.htm
old-project: debugger
ms.assetid: b82c2206-b81d-4ebf-a8fd-c08d7f57ffc9
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: IDebugSymbols3, IDebugSymbols3::AppendSourcePath, AppendSourcePath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IDebugSymbols.AppendSourcePath,IDebugSymbols2.AppendSourcePath,IDebugSymbols3.AppendSourcePath
req.alt-loc: Dbgeng.h
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
req.typenames: *PDOT4_ACTIVITY, DOT4_ACTIVITY
---

# IDebugSymbols3::AppendSourcePath method



## -description
The <b>AppendSourcePath</b>  method appends directories to the source path.



## -syntax

````
HRESULT AppendSourcePath(
  [in] PCSTR Addition
);
````


## -parameters

### -param Addition [in]

Specifies the directories to append to the source path.  This is a string that contains source path elements separated by semicolons (;).  Each source path element can specify either a directory or a source server.


## -returns
<dl>
<dt><b>S_OK</b></dt>
</dl>The method was successful.

 

This method may also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.


## -remarks
The source path is used by the engine when searching for source files.

For more information about manipulating the source path, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560141">Using Source Files</a>.  For an overview of the source path and its syntax, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff556906">Source Path</a>.


## -see-also
<dl>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugsymbols.md">IDebugSymbols</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugsymbols2.md">IDebugSymbols2</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff548358">GetSourcePath</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556781">SetSourcePath</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff548367">GetSourcePathElement</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugSymbols::AppendSourcePath method%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

