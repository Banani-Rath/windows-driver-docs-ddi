---
UID: NF:ntifs.SeReleaseSubjectContext
title: SeReleaseSubjectContext function
author: windows-driver-content
description: The SeReleaseSubjectContext routine releases a subject security context captured by an earlier call to SeCaptureSubjectContext.
old-location: ifsk\sereleasesubjectcontext.htm
old-project: ifsk
ms.assetid: efae077e-2698-4392-ac2a-8f41acdb12a2
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: SeReleaseSubjectContext
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
req.alt-api: SeReleaseSubjectContext
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
req.irql: PASSIVE_LEVEL
req.typenames: TOKEN_TYPE
---

# SeReleaseSubjectContext function



## -description
The <b>SeReleaseSubjectContext</b> routine releases a subject security context captured by an earlier call to <b>SeCaptureSubjectContext</b>.



## -syntax

````
VOID SeReleaseSubjectContext(
  _Inout_ PSECURITY_SUBJECT_CONTEXT SubjectContext
);
````


## -parameters

### -param SubjectContext [in, out]

Pointer to the captured security context.


## -returns
None


## -remarks
File systems must call <b>SeCaptureSubjectContext</b> before performing access validation or generating audit messages. This is necessary to provide a consistent security context to routines such as <b>SeQueryAuthenticationIdToken</b>, <b>SeQuerySubjectContextToken</b>, and <b>SePrivilegeCheck</b>. After these operations have been performed, the captured context should be released as soon as possible by calling <b>SeReleaseSubjectContext</b>.

For more information about security and access control, see the documentation on these topics in the Microsoft Windows SDK.


## -see-also
<dl>
<dt>
<a href="..\ntifs\nf-ntifs-secapturesubjectcontext.md">SeCaptureSubjectContext</a>
</dt>
<dt>
<a href="..\wdm\ns-wdm-_security_subject_context.md">SECURITY_SUBJECT_CONTEXT</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-selocksubjectcontext.md">SeLockSubjectContext</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-seprivilegecheck.md">SePrivilegeCheck</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-sequeryauthenticationidtoken.md">SeQueryAuthenticationIdToken</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-sequerysubjectcontexttoken.md">SeQuerySubjectContextToken</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-seunlocksubjectcontext.md">SeUnlockSubjectContext</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20SeReleaseSubjectContext routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

