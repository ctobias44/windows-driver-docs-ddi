---
UID: NF:netadapter.NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT
title: NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT function (netadapter.h)
description: The NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT function initializes a NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES structure.
tech.root: netvista
ms.date: 10/22/2019
keywords: ["NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT function"]
ms.keywords: NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT
req.header: netadapter.h
req.include-header: netadaptercx.h 
req.target-type: Universal
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: Any level as long as target memory is resident
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: Vb
f1_keywords:
 - NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT
 - netadapter/NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT
product:
 - Windows
---

# NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT function


## -description

The **NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT** function initializes a [**NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES**](../netadapter/ns-netadapter-_net_adapter_power_offload_ns_capabilities.md) structure.

## -parameters

### -param Capabilities

A pointer to a client driver-allocated [**NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES**](../netadapter/ns-netadapter-_net_adapter_power_offload_ns_capabilities.md) structure.

### -param MaximumOffloadCount

The maximum number of NS protocol offloads that the hardware supports.


## -remarks

After calling this function to initialize the **NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES** structure, call [**NetAdapterPowerOffloadSetNsCapabilities**](../netadapter/nf-netadapter-netadapterpoweroffloadsetnscapabilities.md) to set the net adapter's NS protocol offload capabilities. Client drivers typically call **NetAdapterPowerOffloadSetNsCapabilities** when starting a net adapter, but before calling [**NetAdapterStart**](../netadapter/nf-netadapter-netadapterstart.md).

## -see-also

[Configuring power management](/windows-hardware/drivers/netcx/configuring-power-management)

[**NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES**](../netadapter/ns-netadapter-_net_adapter_power_offload_ns_capabilities.md)

[**NetAdapterPowerOffloadSetNsCapabilities**](../netadapter/nf-netadapter-netadapterpoweroffloadsetnscapabilities.md)

[**NetAdapterStart**](../netadapter/nf-netadapter-netadapterstart.md)
