---
UID: NF:ntifs.FsRtlCheckLockForOplockRequest
title: FsRtlCheckLockForOplockRequest function (ntifs.h)
description: The FsRtlCheckLockForOplockRequest routine checks for locks within the allocation size of a file. The file lock object is checked for the presence of byte range locks that would prevent an oplock request from being granted.
old-location: ifsk\fsrtlchecklockforoplockrequest.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["FsRtlCheckLockForOplockRequest function"]
ms.keywords: FsRtlCheckLockForOplockRequest, FsRtlCheckLockForOplockRequest routine [Installable File System Drivers], ifsk.fsrtlchecklockforoplockrequest, ntifs/FsRtlCheckLockForOplockRequest
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 8.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
targetos: Windows
req.typenames: 
ms.custom: RS5
f1_keywords:
 - FsRtlCheckLockForOplockRequest
 - ntifs/FsRtlCheckLockForOplockRequest
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - FsRtlCheckLockForOplockRequest
dev_langs:
 - c++
---

# FsRtlCheckLockForOplockRequest function


## -description

The <b>FsRtlCheckLockForOplockRequest</b> routine checks for locks within the allocation size of a file. The file lock object is  checked for the presence of  byte range locks that would prevent an oplock request from being granted.

## -parameters

### -param FileLock [in]


The file lock that specifies locked ranges.

### -param AllocationSize [in]


The file allocation size to check for any locked ranges.

## -returns

<b>FsRtlCheckLockForOplockRequest</b> returns <b>TRUE</b> if the  oplock request can be granted;  <b> FALSE</b> otherwise.

## -remarks

<b>FsRtlCheckLockForOplockRequest</b> returns <b>TRUE</b> if <i>AllocationSize</i> = 0.

If <i>FileLock</i> has any pending lock requests, the check fails and <b>FsRtlCheckLockForOplockRequest</b> returns <b>FALSE</b>.

