---
UID: NF:ntifs._FSRTL_ADVANCED_FCB_HEADER.FsRtlRemoveLargeMcbEntry~r2
title: FsRtlRemoveLargeMcbEntry function
author: windows-driver-content
description: The FsRtlRemoveLargeMcbEntry routine removes one or more mappings from a map control block (MCB).
old-location: ifsk\fsrtlremovelargemcbentry.htm
old-project: ifsk
ms.assetid: c0608442-59ba-4431-94d5-7514555d0b4f
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: FsRtlRemoveLargeMcbEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: FsRtlRemoveLargeMcbEntry
req.alt-loc: NtosKrnl.exe
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: <= APC_LEVEL
req.typenames: TOKEN_TYPE
---

# FsRtlRemoveLargeMcbEntry function



## -description
The <b>FsRtlRemoveLargeMcbEntry</b> routine removes one or more mappings from a map control block (MCB).



## -syntax

````
VOID FsRtlRemoveLargeMcbEntry(
  _In_ PLARGE_MCB OpaqueMcb,
  _In_ LONGLONG   LargeVbn,
  _In_ LONGLONG   LargeSectorCount
);
````


## -parameters

### -param OpaqueMcb [in]

Pointer to the MCB structure. 


### -param LargeVbn [in]

Starting virtual block number (VBN) of the range for which mappings are to be removed from the MCB. 


### -param LargeSectorCount [in]

Number of sectors (VBNs) in the range for which mappings are to be removed. 


## -returns
None


## -remarks
<b>FsRtlRemoveLargeMcbEntry</b> removes all mappings of VBNs to LBNs in the MCB that fall within the range of VBNs that begins with <i>*LargeVbn</i> and ends with (<i>*LargeVbn </i>+ <i>LargeSectorCount</i> - 1). 

Holes (gaps) between mappings are ignored. 

If the range of VBNs to be removed includes the highest mapped VBN in the MCB, the MCB's <b>PairCount</b> member is adjusted accordingly.

If a pool allocation failure occurs, <b>FsRtlRemoveLargeMcbEntry</b> raises a STATUS_INSUFFICIENT_RESOURCES exception. To gain control if this pool allocation failure occurs, the driver should wrap the call to <b>FsRtlRemoveLargeMcbEntry</b> in a <b>try-except</b> or <b>try-finally</b> statement.


## -see-also
<dl>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtladdlargemcbentry~r3.md">FsRtlAddLargeMcbEntry</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlgetnextlargemcbentry~r4.md">FsRtlGetNextLargeMcbEntry</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlinitializelargemcb~r1.md">FsRtlInitializeLargeMcb</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtllookuplargemcbentry~r6.md">FsRtlLookupLargeMcbEntry</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtllookuplastlargemcbentry~r2.md">FsRtlLookupLastLargeMcbEntry</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtllookuplastlargemcbentryandindex~r3.md">FsRtlLookupLastLargeMcbEntryAndIndex</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlnumberofrunsinlargemcb.md">FsRtlNumberOfRunsInLargeMcb</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlsplitlargemcb~r2.md">FsRtlSplitLargeMcb</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtltruncatelargemcb~r1.md">FsRtlTruncateLargeMcb</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtluninitializelargemcb.md">FsRtlUninitializeLargeMcb</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FsRtlRemoveLargeMcbEntry routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

