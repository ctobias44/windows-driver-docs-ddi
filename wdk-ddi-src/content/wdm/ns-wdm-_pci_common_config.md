---
UID: NS:wdm._PCI_COMMON_CONFIG
title: _PCI_COMMON_CONFIG (wdm.h)
description: The _PCI_COMMON_CONFIG structure (wdm.h) defines standard PCI configuration information.
old-location: kernel\pci_common_config.htm
tech.root: kernel
ms.date: 12/01/2021
keywords: ["PCI_COMMON_CONFIG structure"]
ms.keywords: "*PPCI_COMMON_CONFIG, PCI_COMMON_CONFIG, PCI_COMMON_CONFIG structure [Kernel-Mode Driver Architecture], PPCI_COMMON_CONFIG, PPCI_COMMON_CONFIG structure pointer [Kernel-Mode Driver Architecture], _PCI_COMMON_CONFIG, kernel.pci_common_config, kstruct_c_42f21057-e812-4a4d-96c5-f1177a03982b.xml, wdm/PCI_COMMON_CONFIG, wdm/PPCI_COMMON_CONFIG"
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h
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
req.typenames: PCI_COMMON_CONFIG, *PPCI_COMMON_CONFIG
f1_keywords:
 - _PCI_COMMON_CONFIG
 - wdm/_PCI_COMMON_CONFIG
 - PPCI_COMMON_CONFIG
 - wdm/PPCI_COMMON_CONFIG
 - PCI_COMMON_CONFIG
 - wdm/PCI_COMMON_CONFIG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdm.h
api_name:
 - _PCI_COMMON_CONFIG
 - PPCI_COMMON_CONFIG
 - PCI_COMMON_CONFIG
---

# _PCI_COMMON_CONFIG structure (wdm.h)

## -description

The **PCI_COMMON_CONFIG** structure defines standard PCI configuration information returned by the [HalGetBusData](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85)) or [HalGetBusDataByOffset](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85)) routine for the input *BusDataType* PCIConfiguration, assuming the caller-allocated *Buffer* is of sufficient *Length*.

## -struct-fields

### -field DeviceSpecific

Contains any device-specific initialization information that is available.

### -field PCI_COMMON_HEADER

### -field BIST

Zero indicates that the device does not support built-in self-test. Otherwise, the device supports built-in self-test according to the PCI standard.

### -field BaseClass

Identifies type of the device, according to the PCI classification scheme.

### -field CacheLineSize

Contains the system cache line size in 32-bit units. This member is relevant only for PCI bus-master devices. The system determines this value during the boot process.

### -field Command

Accesses the PCI device's control register. Writing a zero to this register renders the device logically disconnected from the PCI bus except for configuration access. Otherwise, the functionality of the register is device-dependent. Possible system-defined bit encodings for this member include:

PCI_ENABLE_IO_SPACE

PCI_ENABLE_MEMORY_SPACE

PCI_ENABLE_BUS_MASTER

PCI_ENABLE_SPECIAL_CYCLES

PCI_ENABLE_WRITE_AND_VALIDATE

PCI_ENABLE_VGA_COMPATIBLE_PALETTE

PCI_ENABLE_PARITY

PCI_ENABLE_WAIT_CYCLE

PCI_ENABLE_SERR

PCI_ENABLE_FAST_BACK_TO_BACK

### -field DeviceID

Identifies the particular device. This value is assigned by the manufacturer.

### -field HeaderType

The system ORs the value of this member with PCI_MULTIFUNCTION, if appropriate to the device. The value of this member indicates the PCI_HEADER_TYPE_0 layout that follows.

### -field LatencyTimer

Contains the value of the latency timer in units of PCI bus clocks. This member is relevant only for PCI bus-master devices. The system determines this value during the boot process.

### -field ProgIf

Identifies the register-level programming interface, if any, for the device, according to the PCI classification scheme.

### -field RevisionID

Specifies the revision level of the device described by the **DeviceID** member. This value is assigned by the manufacturer.

### -field Status

Accesses the PCI device's status register. The functionality of this register is device-dependent. Possible system-defined bit encodings for this member include:

PCI_STATUS_FAST_BACK_TO_BACK             // read-only

PCI_STATUS_DATA_PARITY_DETECTED

PCI_STATUS_DEVSEL                        // 2 bits wide

PCI_STATUS_SIGNALED_TARGET_ABORT

PCI_STATUS_RECEIVED_TARGET_ABORT

PCI_STATUS_RECEIVED_MASTER_ABORT

PCI_STATUS_SIGNALED_SYSTEM_ERROR

PCI_STATUS_DETECTED_PARITY_ERROR

### -field SubClass

Identifies the subtype, if any, of the device, according to the PCI classification scheme.

### -field VendorID

Identifies the manufacturer of the device. This must be a value allocated by the PCI SIG.

### -field u

#### type0

Drivers call [HalAssignSlotResources](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85)) to configure these values and to get back the bus-relative values passed to other configuration routines.

##### BaseAddresses

Base addresses.

##### Reserved1

Reserved.

##### ROMBaseAddress

ROM base address.

##### Reserved2

Reserved.

##### InterruptLine

Interrupt line number.

##### InterruptPin

Interrupt pin number.

##### MinimumGrant

Minimum grant.

##### MaximumLatency

Maximum latency.

##### - u.type0

Drivers call [HalAssignSlotResources](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85)) to configure these values and to get back the bus-relative values passed to other configuration routines.

##### type0.BaseAddresses

Base addresses.

##### type0.Reserved1

Reserved.

##### type0.ROMBaseAddress

ROM base address.

##### type0.Reserved2

Reserved.

##### type0.InterruptLine

Interrupt line number.

##### type0.InterruptPin

Interrupt pin number.

##### type0.MinimumGrant

Minimum grant.

##### type0.MaximumLatency

Maximum latency.

###### - u.type0.BaseAddresses

Base addresses.

###### - u.type0.InterruptLine

Interrupt line number.

###### - u.type0.InterruptPin

Interrupt pin number.

###### - u.type0.MaximumLatency

Maximum latency.

###### - u.type0.MinimumGrant

Minimum grant.

###### - u.type0.ROMBaseAddress

ROM base address.

###### - u.type0.Reserved1

Reserved.

###### - u.type0.Reserved2

Reserved.

## -remarks

Certain members of this structure have read-only values, so attempts to reset them are ignored. These members include the following: **VendorID**, **DeviceID**, **RevisionID**, **ProgIf**, **SubClass**, **BaseClass**, **HeaderType**, **InterruptPin**, **MinimumGrant**, and **MaximumLatency.**

Other members are provisionally read-only: that is, the system initializes them to their correct values, so drivers can safely treat them as read-only. However, they can be reset if a bus-master driver finds it necessary. These members include the following: **CacheLineSize** and **LatencyTimer**.

## -see-also

[HalAssignSlotResources](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))

[HalGetBusData](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))

[HalGetBusDataByOffset](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))

[HalSetBusData](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))

[HalSetBusDataByOffset](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))
