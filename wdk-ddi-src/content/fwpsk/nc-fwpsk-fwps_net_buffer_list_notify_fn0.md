---
UID: NC:fwpsk.FWPS_NET_BUFFER_LIST_NOTIFY_FN0
title: FWPS_NET_BUFFER_LIST_NOTIFY_FN0
author: windows-driver-content
description: The filter engine calls the FWPS_NET_BUFFER_LIST_NOTIFY_FN0 callout function to notify the callout driver about events that are associated with packets tagged by the callout.Note  FWPS_NET_BUFFER_LIST_NOTIFY_FN0 is the specific version of FWPS_NET_BUFFER_LIST_NOTIFY_FN used in Windows 7 and later. See WFP Version-Independent Names and Targeting Specific Versions of Windows for more information. For Windows 8, FWPS_NET_BUFFER_LIST_NOTIFY_FN1 is available.
old-location: netvista\fwps_net_buffer_list_notify_fn0.htm
old-project: netvista
ms.assetid: ad603c9c-aa11-4c8b-9d19-be2938608f3d
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: FwpmEngineOpen0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: fwpsk.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 7.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: FwpsNetBufferListNotifyFN0
req.alt-loc: fwpsk.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: <= DISPATCH_LEVEL
req.typenames: PINSTANCE_PARTIAL_INFORMATION, INSTANCE_PARTIAL_INFORMATION
---

# FWPS_NET_BUFFER_LIST_NOTIFY_FN0 callback



## -description
The filter engine calls the 
  <i>FWPS_NET_BUFFER_LIST_NOTIFY_FN0</i> callout function to notify the callout driver about events that are
  associated with packets tagged by the callout.



## -prototype

````
FWPS_NET_BUFFER_LIST_NOTIFY_FN0 FwpsNetBufferListNotifyFN0;

void NTAPI FwpsNetBufferListNotifyFN0(
  _In_        FWPS_NET_BUFFER_LIST_EVENT_TYPE0 eventType,
  _Inout_opt_ NET_BUFFER_LIST                  *netBufferList,
  _Inout_opt_ NET_BUFFER_LIST                  *newNetBufferList,
  _In_        UINT16                           layerId,
  _In_        UINT64                           context,
  _In_        UINT64                           contextTag
)
{ ... }
````


## -parameters

### -param eventType [in]

A value that indicates the type of notification that the filter engine is sending to the callout.
     This parameter will be set to one of the values of the 
     <a href="..\fwpsk\ne-fwpsk-fwps_net_buffer_list_event_type0_.md">
     FWPS_NET_BUFFER_LIST_EVENT_TYPE0</a> enumeration.


### -param netBufferList [in, out, optional]

A pointer to the buffer list that contains packets that were previously tagged as interesting by
     the callout driver.


### -param newNetBufferList [in, out, optional]

A pointer to an updated buffer list that contains packets that are interesting to the callout
     driver. The use of this parameter differs depending on the type of event. For events where a change is
     made to the indicated packet, the changed version is passed as this parameter.


### -param layerId [in]

The layer from which the notification function was called.


### -param context [in]

The context used to tag the packets of interest. This value is the value assigned to the packet by
     the callout driver and is used to identify the packet.


### -param contextTag [in]

The context tag used to associate the packets of interest with the context of the callout
     driver.


## -returns
None.


## -remarks
This function is associated with a callout driver by a call to 
    <a href="..\fwpsk\nf-fwpsk-fwpsnetbufferlistassociatecontext0.md">
    FwpsNetBufferListAssociateContext0</a>. A callout driver can use a single notification function to
    handle messages for multiple associated buffer lists by using the context and context tag to
    differentiate between instances.


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>
</dt>
<dt>
<a href="..\fwpsk\ns-fwpsk-fwps_callout0_.md">FWPS_CALLOUT0</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff552389">FWPS_FILTER1</a>
</dt>
<dt>
<a href="..\fwpsk\nc-fwpsk-fwps_net_buffer_list_notify_fn1.md">
  FWPS_NET_BUFFER_LIST_NOTIFY_FN1</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpscalloutregister1.md">FwpsCalloutRegister1</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543875">Callout Driver Callout Functions</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/a151256b-d69f-4abb-bf68-644f157dfdd7">Using Packet Tagging</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FWPS_NET_BUFFER_LIST_NOTIFY_FN0 callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

