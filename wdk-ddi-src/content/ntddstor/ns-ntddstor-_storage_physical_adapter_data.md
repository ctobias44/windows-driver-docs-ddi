---
UID: NS:ntddstor._STORAGE_PHYSICAL_ADAPTER_DATA
title: _STORAGE_PHYSICAL_ADAPTER_DATA (ntddstor.h)
description: Specifies the physical device data of a storage adapter.
old-location: storage\storage_physical_adapter_data.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["STORAGE_PHYSICAL_ADAPTER_DATA structure"]
ms.keywords: "*PSTORAGE_PHYSICAL_ADAPTER_DATA, PSTORAGE_PHYSICAL_ADAPTER_DATA, PSTORAGE_PHYSICAL_ADAPTER_DATA structure pointer [Storage Devices], STORAGE_PHYSICAL_ADAPTER_DATA, STORAGE_PHYSICAL_ADAPTER_DATA structure [Storage Devices], _STORAGE_PHYSICAL_ADAPTER_DATA, ntddstor/PSTORAGE_PHYSICAL_ADAPTER_DATA, ntddstor/STORAGE_PHYSICAL_ADAPTER_DATA, storage.storage_physical_adapter_data"
req.header: ntddstor.h
req.include-header: Ntddstor.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: STORAGE_PHYSICAL_ADAPTER_DATA, *PSTORAGE_PHYSICAL_ADAPTER_DATA
f1_keywords:
 - _STORAGE_PHYSICAL_ADAPTER_DATA
 - ntddstor/_STORAGE_PHYSICAL_ADAPTER_DATA
 - PSTORAGE_PHYSICAL_ADAPTER_DATA
 - ntddstor/PSTORAGE_PHYSICAL_ADAPTER_DATA
 - STORAGE_PHYSICAL_ADAPTER_DATA
 - ntddstor/STORAGE_PHYSICAL_ADAPTER_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntddstor.h
api_name:
 - _STORAGE_PHYSICAL_ADAPTER_DATA
 - PSTORAGE_PHYSICAL_ADAPTER_DATA
 - STORAGE_PHYSICAL_ADAPTER_DATA
---

# _STORAGE_PHYSICAL_ADAPTER_DATA structure


## -description

Specifies the physical device data of a storage adapter.

## -struct-fields

### -field AdapterId

The hardware ID of the storage adapter.

### -field HealthStatus

Indicates the health status of a storage adapter, of type <a href="/windows-hardware/drivers/ddi/ntddstor/ne-ntddstor-_storage_component_health_status">STORAGE_COMPONENT_HEALTH_STATUS</a>.

### -field CommandProtocol

Specifies the storage command protocols that are used between software and hardware, of type <a href="/windows-hardware/drivers/ddi/ntddstor/ne-ntddstor-_storage_protocol_type">STORAGE_PROTOCOL_TYPE</a>.

### -field SpecVersion

Indicates the specification of the storage adapter, of type <a href="/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_spec_version">STORAGE_SPEC_VERSION</a>.

### -field Vendor

### -field Model

### -field FirmwareRevision

### -field PhysicalLocation

### -field ExpanderConnected

### -field Reserved0

### -field Reserved1

 




### -field ExpandedConnector

Specifies if the storage adapter includes an expanded connector.


### -field FirmwareRevision[16]

The revision number of the storage adapter.


### -field Model[40]

The model name of the storage adapter.


### -field PhysicalLocation[32]

This member is reserved for future use.


### -field Reserved0[3]

Specifies if the storage adapter is reserved.


### -field Reserved1[3]

Specifies if the storage adapter is reserved.


### -field Vendor[8]

The vendor name of the storage adapter.

