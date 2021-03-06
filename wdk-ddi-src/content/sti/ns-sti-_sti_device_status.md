---
UID: NS:sti._STI_DEVICE_STATUS
title: _STI_DEVICE_STATUS
author: windows-driver-content
description: The STI_DEVICE_STATUS structure is used as a parameter to the IStiDevice::GetStatus and IStiUSD::GetStatus methods.
old-location: image\sti_device_status.htm
old-project: image
ms.assetid: 40104e1f-b936-430b-9e8c-28738579f4c7
ms.author: windowsdriverdev
ms.date: 1/17/2018
ms.keywords: _STI_DEVICE_STATUS, STI_DEVICE_STATUS, *PSTI_DEVICE_STATUS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: sti.h
req.include-header: Sti.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: STI_DEVICE_STATUS
req.alt-loc: sti.h
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
req.typenames: STI_DEVICE_STATUS, *PSTI_DEVICE_STATUS
req.product: Windows 10 or later.
---

# _STI_DEVICE_STATUS structure



## -description
The STI_DEVICE_STATUS structure is used as a parameter to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543752">IStiDevice::GetStatus</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff543823">IStiUSD::GetStatus</a> methods.



## -syntax

````
typedef struct _STI_DEVICE_STATUS {
  DWORD dwSize;
  DWORD StatusMask;
  DWORD dwOnlineState;
  DWORD dwHardwareStatusCode;
  DWORD dwEventHandlingState;
  DWORD dwPollingInterval;
} STI_DEVICE_STATUS, *PSTI_DEVICE_STATUS;
````


## -struct-fields

### -field dwSize

Caller-supplied size, in bytes, of the STI_DEVICE_STATUS structure.


### -field StatusMask

One or more caller-supplied bit flags, indicating the type of status information being requested. The following flags are defined:

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
STI_DEVSTATUS_EVENTS_STATE

</td>
<td>
The driver should fill in the <b>dwEventHandlingState</b> member.

</td>
</tr>
<tr>
<td>
STI_DEVSTATUS_ONLINE_STATE 

</td>
<td>
The driver should fill in the <b>dwOnlineState</b> member.

</td>
</tr>
</table>
 


### -field dwOnlineState

Bit flags indicating the device's current status. The following flags are defined in <i>Sti.h</i>.

Currently use of STI_ONLINESTATE_OPERATIONAL is required, while use of all other flags is optional. (Currently, STI_ONLINESTATE_OPERATIONAL is the only flag that the still image server checks.)




### -field STI_ONLINESTATE_BUSY

The device is busy.

</dd>
</dl>



### -field STI_ONLINESTATE_ERROR

The device has reported an error.

</dd>
</dl>



### -field STI_ONLINESTATE_INITIALIZING

The device is being initialized.

</dd>
</dl>



### -field STI_ONLINESTATE_IO_ACTIVE

The device is active but not accepting commands.

</dd>
</dl>



### -field STI_ONLINESTATE_OFFLINE

The device is off-line.

</dd>
</dl>



### -field STI_ONLINESTATE_OPERATIONAL

The device is online and ready. If set, Control Panel indicates the device is ready. Otherwise, it indicates the device is off-line.

</dd>
</dl>



### -field STI_ONLINESTATE_PAPER_JAM

The device has reported a paper jam.

</dd>
</dl>



### -field STI_ONLINESTATE_PAPER_PROBLEM

The device has reported an unspecified paper problem.

</dd>
</dl>



### -field STI_ONLINESTATE_PAUSED

The device is paused.

</dd>
</dl>



### -field STI_ONLINESTATE_PENDING

I/O operations are pending.

</dd>
</dl>



### -field STI_ONLINESTATE_POWER_SAVE

The device is in power save mode.

</dd>
</dl>



### -field STI_ONLINESTATE_TRANSFERRING

The device is transferring data.

</dd>
</dl>



### -field STI_ONLINESTATE_USER_INTERVENTION

The device requires user intervention.

</dd>
</dl>



### -field STI_ONLINESTATE_WARMING_UP

The device is warming up.

</dd>
</dl>

### -field dwHardwareStatusCode

Optional device-specific, vendor-defined value.


### -field dwEventHandlingState

Contains bit flags indicating event status. The following flags are defined in <i>Sti.h</i>.




### -field STI_EVENTHANDLING_ENABLED

<i>Not used</i>.

</dd>
</dl>



### -field STI_EVENTHANDLING_PENDING

A device event has occurred.

</dd>
</dl>



### -field STI_EVENTHANDLING_POLLING

<i>Not used</i>.

</dd>
</dl>

### -field dwPollingInterval

Time value, in milliseconds, indicating how often the device should be polled, if polling is required.


## -remarks
