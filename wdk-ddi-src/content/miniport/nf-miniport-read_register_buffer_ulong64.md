---
UID: NF:miniport.READ_REGISTER_BUFFER_ULONG64
title: READ_REGISTER_BUFFER_ULONG64 function (miniport.h)
description: The READ_REGISTER_BUFFER_ULONG64 function (miniport.h) reads a number of ULONG64 values from the specified register address into a buffer.
old-location: wdf\read_register_buffer_ulong64.htm
tech.root: wdf
ms.date: 02/26/2018
keywords: ["READ_REGISTER_BUFFER_ULONG64 function"]
ms.keywords: READ_REGISTER_BUFFER_ULONG64, READ_REGISTER_BUFFER_ULONG64 function, umdf.read_register_buffer_ulong64, wdf.read_register_buffer_ulong64, wudfddi_hwaccess/READ_REGISTER_BUFFER_ULONG64
req.header: miniport.h
req.include-header: Wdm.h, Miniport.h, Wudfwdm.h
req.target-type: Desktop
req.target-min-winverclnt: 64-bit Windows
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MEMORY_CACHING_TYPE
f1_keywords:
 - READ_REGISTER_BUFFER_ULONG64
 - miniport/READ_REGISTER_BUFFER_ULONG64
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wudfddi_hwaccess.h
api_name:
 - READ_REGISTER_BUFFER_ULONG64
---

# READ_REGISTER_BUFFER_ULONG64 function (miniport.h)


## -description

<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>READ_REGISTER_BUFFER_ULONG64</b> function reads a number of ULONG64 values from the specified register address into a buffer.

## -parameters

### -param Register [in]


A pointer to the register, which must be a mapped range in memory space.

### -param Buffer [out]


A pointer to a buffer into which an array of ULONG64 values is read.

### -param Count [in]


Specifies the number of ULONG64 values to be read into the buffer.


### -param pDevice [in]

Specifies a pointer to the <a href="..\wudfddi\nn-wudfddi-iwdfdevice3.md">IWDFDevice3</a> interface for the device object of the device to access.

## -syntax

```cpp
void READ_REGISTER_BUFFER_ULONG64(
  _In_  IWDFDevice3 *pDevice,
  _In_  PULONG64    Register,
  _Out_ PULONG64    Buffer,
  _In_  ULONG       Count
);
```

## -remarks

For more information, see <a href="/windows-hardware/drivers/wdf/reading-and-writing-to-device-registers-in-umdf-1-x-drivers">Reading and Writing to Device Registers in UMDF 1.x Drivers</a>.
