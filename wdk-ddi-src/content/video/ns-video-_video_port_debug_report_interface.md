---
UID: NS:video._VIDEO_PORT_DEBUG_REPORT_INTERFACE
title: _VIDEO_PORT_DEBUG_REPORT_INTERFACE
author: windows-driver-content
description: The VIDEO_PORT_DEBUG_REPORT_INTERFACE structure holds pointers to the Debug Report functions, which are implemented by the video port driver.
old-location: display\video_port_debug_report_interface.htm
old-project: display
ms.assetid: 11536f1e-523c-4796-a973-e53291c756a8
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: _VIDEO_PORT_DEBUG_REPORT_INTERFACE, VIDEO_PORT_DEBUG_REPORT_INTERFACE, *PVIDEO_PORT_DEBUG_REPORT_INTERFACE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: video.h
req.include-header: Video.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: VIDEO_PORT_DEBUG_REPORT_INTERFACE
req.alt-loc: video.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: See Remarks section.
req.typenames: VIDEO_PORT_DEBUG_REPORT_INTERFACE, *PVIDEO_PORT_DEBUG_REPORT_INTERFACE
req.product: Windows 10 or later.
---

# _VIDEO_PORT_DEBUG_REPORT_INTERFACE structure



## -description
The VIDEO_PORT_DEBUG_REPORT_INTERFACE structure holds pointers to the Debug Report functions, which are implemented by the video port driver.



## -syntax

````
typedef struct _VIDEO_PORT_DEBUG_REPORT_INTERFACE {
  USHORT                 Size;
  USHORT                 Version;
  PVOID                  Context;
  PINTERFACE_REFERENCE   InterfaceReference;
  PINTERFACE_DEREFERENCE InterfaceDereference;
  PVIDEO_DEBUG_REPORT    (*DbgReportCreate)(
      _In_ PVOID HwDeviceExtension, 
      _In_ ULONG ulCode, 
      _In_ ULONG_PTR ulpArg1, 
      _In_ ULONG_PTR ulpArg2, 
      _In_ ULONG_PTR ulpArg3, 
      _In_ ULONG_PTR ulpArg4);
  BOOLEAN                (*DbgReportSecondaryData)(
      _In_ PVIDEO_DEBUG_REPORT pReport, 
      _In_ PVOID pvData, 
      _In_ ULONG ulDataSize);
  VOID                   (*DbgReportComplete)(_Inout_opt_ PVIDEO_DEBUG_REPORT pReport);
} VIDEO_PORT_DEBUG_REPORT_INTERFACE, *PVIDEO_PORT_DEBUG_REPORT_INTERFACE;
````


## -struct-fields

### -field Size

Specifies the size, in bytes, of this structure.


### -field Version

Specifies the version of the interface returned by the video port driver. Currently, the only supported version is VIDEO_PORT_DEBUG_REPORT_INTERFACE_VERSION_1.


### -field Context

Pointer to a context that is provided by the video port driver.


### -field InterfaceReference

Pointer to an interface reference function that is implemented by the video port driver.


### -field InterfaceDereference

Pointer to an interface dereference function that is implemented by the video port driver.


### -field DbgReportCreate

Pointer to the video port driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff549088">DbgReportCreate</a> function. 


### -field DbgReportSecondaryData

Pointer to the video port driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff549099">DbgReportSecondaryData</a> function. 


### -field DbgReportComplete

Pointer to the video port driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff549080">DbgReportComplete</a> function. 


## -remarks
This structure is available in the following operating systems:

Windows Server 2003 SP1 and subsequent service packs

Windows XP SP2 and subsequent service packs

The video miniport driver supplies the <b>Size</b> and <b>Version</b> members of this structure, and then calls <a href="..\video\nf-video-videoportqueryservices.md">VideoPortQueryServices</a>, which initializes the remaining members of this structure.


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549088">DbgReportCreate</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549099">DbgReportSecondaryData</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549080">DbgReportComplete</a>
</dt>
<dt>
<a href="..\video\nf-video-videoportqueryservices.md">VideoPortQueryServices</a>
</dt>
<dt>
<a href="..\wdm\ns-wdm-_interface.md">INTERFACE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20VIDEO_PORT_DEBUG_REPORT_INTERFACE structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

