---
UID: NF:ntifs.ZwQuerySecurityObject
title: ZwQuerySecurityObject function (ntifs.h)
description: The ZwQuerySecurityObject routine retrieves a copy of an object's security descriptor. A security descriptor can be in absolute or self-relative form.
old-location: kernel\zwquerysecurityobject.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["ZwQuerySecurityObject function"]
ms.keywords: NtQuerySecurityObject, ZwQuerySecurityObject, ZwQuerySecurityObject routine [Kernel-Mode Driver Architecture], k111_50bbb447-b993-4020-a8d7-e54f0b31e84e.xml, kernel.zwquerysecurityobject, ntifs/NtQuerySecurityObject, ntifs/ZwQuerySecurityObject
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows XP and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: PowerIrpDDis, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - ZwQuerySecurityObject
 - ntifs/ZwQuerySecurityObject
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - ZwQuerySecurityObject
---

# ZwQuerySecurityObject function


## -description

The **ZwQuerySecurityObject** routine retrieves a copy of an object's security descriptor.

## -parameters

### -param Handle [in]

Handle for the object whose security descriptor is to be queried. This handle must have the access specified in the Meaning column of the table shown in the description of the **SecurityInformation** parameter.

### -param SecurityInformation [in]

A [**SECURITY_INFORMATION**](/windows-hardware/drivers/ifs/security-information) value specifying the information to be queried as a combination of one or more of the following.

| Value | Meaning |
| ----- | ------- |
| OWNER_SECURITY_INFORMATION | The object's owner identifier is being queried. Requires READ_CONTROL access. |
| GROUP_SECURITY_INFORMATION | The object's primary group identifier is being queried. Requires READ_CONTROL access. |
| SACL_SECURITY_INFORMATION | The object's system ACL (SACL) is being queried. Requires ACCESS_SYSTEM_SECURITY access. |
| DACL_SECURITY_INFORMATION | The object's discretionary access control list (DACL) is being queried. Requires READ_CONTROL access. |

### -param SecurityDescriptor [out]

Caller-allocated buffer that **ZwQuerySecurityObject** fills with a copy of the specified security descriptor. The [**SECURITY_DESCRIPTOR**](ns-ntifs-_security_descriptor.md) structure is returned in self-relative format.

### -param Length [in]

Size, in bytes, of the buffer pointed to by **SecurityDescriptor**.

### -param LengthNeeded [out]

Pointer to a caller-allocated variable that receives the number of bytes required to store the copied security descriptor.

## -returns

**ZwQuerySecurityObject** returns STATUS_SUCCESS or an appropriate error status. Possible error status codes include the following:

| Return code | Description |
| ----------- | ----------- |
| STATUS_ACCESS_DENIED | **Handle** did not have the required access. |
| STATUS_BUFFER_TOO_SMALL | The buffer is too small for the security descriptor. None of the security information was copied to the buffer. |
| STATUS_INVALID_HANDLE | **Handle** was not a valid handle. |
| STATUS_OBJECT_TYPE_MISMATCH | **Handle** was not a handle of the expected type. |

## -remarks

A security descriptor can be in absolute or self-relative form. In self-relative form, all members of the structure are located contiguously in memory. In absolute form, the structure only contains pointers to the members. For more information, see [Absolute and Self-Relative Security Descriptors](/windows/win32/secauthz/absolute-and-self-relative-security-descriptors).

The NTFS file system imposes a 64K limit on the size of the security descriptor that is written to disk for a file. (The FAT file system does not support security descriptors for files.) Thus a 64K **SecurityDescriptor** buffer is guaranteed to be large enough to hold the returned **SECURITY_DESCRIPTOR** structure.

For more information about security and access control, see the documentation on these topics in the Windows SDK.

Minifilters should call [**FltQuerySecurityObject**](../fltkernel/nf-fltkernel-fltquerysecurityobject.md) instead of **ZwQuerySecurityObject**.

> [!NOTE]
> If the call to the **ZwQuerySecurityObject** function occurs in user mode, you should use the name "**NtQuerySecurityObject**" instead of "**ZwQuerySecurityObject**".

For calls from kernel-mode drivers, the **Nt*Xxx*** and **Zw*Xxx*** versions of a Windows Native System Services routine can behave differently in the way that they handle and interpret input parameters. For more information about the relationship between the **Nt*Xxx*** and **Zw*Xxx*** versions of a routine, see [Using Nt and Zw Versions of the Native System Services Routines](/windows-hardware/drivers/kernel/using-nt-and-zw-versions-of-the-native-system-services-routines).

## -see-also

[**FltQuerySecurityObject**](../fltkernel/nf-fltkernel-fltquerysecurityobject.md)

[**SECURITY_DESCRIPTOR**](ns-ntifs-_security_descriptor.md)

[**SECURITY_INFORMATION**](/windows-hardware/drivers/ifs/security-information)

[**ZwSetSecurityObject**](nf-ntifs-zwsetsecurityobject.md)

