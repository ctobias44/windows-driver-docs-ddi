---
UID: NS:wdm._REG_QUERY_KEY_NAME
title: _REG_QUERY_KEY_NAME (wdm.h)
description: The REG_QUERY_KEY_NAME structure describes the full registry key name of an object being queried.
old-location: kernel\reg_query_key_name.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["REG_QUERY_KEY_NAME structure"]
ms.keywords: "*PREG_QUERY_KEY_NAME, PREG_QUERY_KEY_NAME, PREG_QUERY_KEY_NAME structure pointer [Kernel-Mode Driver Architecture], REG_QUERY_KEY_NAME, REG_QUERY_KEY_NAME structure [Kernel-Mode Driver Architecture], _REG_QUERY_KEY_NAME, kernel.reg_query_key_name, wdm/PREG_QUERY_KEY_NAME, wdm/REG_QUERY_KEY_NAME"
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Windows
req.target-min-winverclnt: Available on Microsoft Windows 10 and later versions of the Windows operating system.
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: REG_QUERY_KEY_NAME, *PREG_QUERY_KEY_NAME
f1_keywords:
 - _REG_QUERY_KEY_NAME
 - wdm/_REG_QUERY_KEY_NAME
 - PREG_QUERY_KEY_NAME
 - wdm/PREG_QUERY_KEY_NAME
 - REG_QUERY_KEY_NAME
 - wdm/REG_QUERY_KEY_NAME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - _REG_QUERY_KEY_NAME
 - PREG_QUERY_KEY_NAME
 - REG_QUERY_KEY_NAME
---

# _REG_QUERY_KEY_NAME structure


## -description

The <b>REG_QUERY_KEY_NAME</b> structure describes the full registry key name
              of an object being queried.

## -struct-fields

### -field Object

A pointer to the registry key object for the key whose metadata is about to be queried.

### -field ObjectNameInfo

A pointer to an <b>OBJECT_NAME_INFORMATION</b> structure (see wdm.h) that contains the full registry key name to be returned by the system, as a Unicode string.

### -field Length

Specifies the size, in bytes, of the <b>ObjectNameInfo</b> buffer.

### -field ReturnLength

### -field CallContext

Optional driver-defined context information that the driver's <a href="/windows-hardware/drivers/ddi/wdm/nc-wdm-ex_callback_function">RegistryCallback</a> routine can supply.

### -field ObjectContext

A pointer to driver-defined context information that the driver has associated with a registry object by calling <a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-cmsetcallbackobjectcontext">CmSetCallbackObjectContext</a>. It contains the key context for the key that is being queried.

### -field Reserved

This member is reserved for future use. 


### -field ResultLength

Pointer to a variable that receives (from the system) the amount of valid data, in bytes, in the <b>ObjectNameInfo</b> buffer.

## -remarks

The system passes this structure to the <a href="/windows-hardware/drivers/ddi/wdm/nc-wdm-ex_callback_function">RegistryCallback</a> routine every time a thread attempts to query the full name of the registry key. 

For more information about registry filtering operations, see <a href="/windows-hardware/drivers/kernel/filtering-registry-calls">Filtering Registry Calls</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/ne-wdm-_reg_notify_class">REG_NOTIFY_CLASS</a>



<a href="/windows-hardware/drivers/ddi/wdm/nc-wdm-ex_callback_function">RegistryCallback</a>

