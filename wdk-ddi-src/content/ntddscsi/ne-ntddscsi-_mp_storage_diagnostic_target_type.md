---
UID: NE:ntddscsi._MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
title: _MP_STORAGE_DIAGNOSTIC_TARGET_TYPE (ntddscsi.h)
description: The MP_STORAGE_DIAGNOSTIC_TARGET_TYPE enumeration specifies the target type of a storage diagnostic.
old-location: storage\mp_storage_diagnostic_target_type.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["MP_STORAGE_DIAGNOSTIC_TARGET_TYPE enumeration"]
ms.keywords: "*PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE, MP_STORAGE_DIAGNOSTIC_TARGET_TYPE, MP_STORAGE_DIAGNOSTIC_TARGET_TYPE enumeration [Storage Devices], PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE, PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE enumeration pointer [Storage Devices], StorageDiagnosticTargetTypeHbaFirmware, StorageDiagnosticTargetTypeMax, StorageDiagnosticTargetTypeMiniport, StorageDiagnosticTargetTypePort, StorageDiagnosticTargetTypeUndefined, _MP_STORAGE_DIAGNOSTIC_TARGET_TYPE, ntddscsi/MP_STORAGE_DIAGNOSTIC_TARGET_TYPE, ntddscsi/PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE, ntddscsi/StorageDiagnosticTargetTypeHbaFirmware, ntddscsi/StorageDiagnosticTargetTypeMax, ntddscsi/StorageDiagnosticTargetTypeMiniport, ntddscsi/StorageDiagnosticTargetTypePort, ntddscsi/StorageDiagnosticTargetTypeUndefined, storage.mp_storage_diagnostic_target_type"
req.header: ntddscsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 10, version 1709.
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
req.typenames: MP_STORAGE_DIAGNOSTIC_TARGET_TYPE, *PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE
f1_keywords:
 - _MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
 - ntddscsi/_MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
 - PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE
 - ntddscsi/PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE
 - MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
 - ntddscsi/MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddscsi.h
api_name:
 - _MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
 - PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE
 - MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
---

# _MP_STORAGE_DIAGNOSTIC_TARGET_TYPE enumeration


## -description

The <b>MP_STORAGE_DIAGNOSTIC_TARGET_TYPE</b> enumeration specifies the target type of a storage diagnostic.

## -enum-fields

### -field MpStorageDiagnosticTargetTypeUndefined

### -field MpStorageDiagnosticTargetTypeMiniport

### -field MpStorageDiagnosticTargetTypeHbaFirmware

### -field MpStorageDiagnosticTargetTypeMax

### -field StorageDiagnosticTargetTypeHbaFirmware

Specifies the target type is a Hba Firmware driver.


### -field StorageDiagnosticTargetTypeMax

Specifies the target type is a Max driver.


### -field StorageDiagnosticTargetTypeMiniport

Specifies the target type is a Miniport driver.


### -field StorageDiagnosticTargetTypePort

Specifies the target type is a port driver.


### -field StorageDiagnosticTargetTypeUndefined

Specifies the target type is undefined.

