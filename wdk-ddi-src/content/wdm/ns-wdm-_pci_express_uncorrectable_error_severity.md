---
UID: NS:wdm._PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
title: _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY (wdm.h)
description: The _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure (wdm.h) describes a PCI Express (PCIe) uncorrectable error severity register.
old-location: pci\pci_express_uncorrectable_error_severity.htm
tech.root: PCI
ms.date: 02/24/2018
keywords: ["PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure"]
ms.keywords: "*PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, PCI.pci_express_uncorrectable_error_severity, PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY union [Buses], PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY union pointer [Buses], _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, pci_struct_49aec790-2c99-489c-b0ca-0653ebe5b52c.xml, wdm/PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, wdm/PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY"
req.header: wdm.h
req.include-header: Ntddk.h, Wdm.h, Miniport.h
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
req.irql: PASSIVE_LEVEL (see Remarks section)
targetos: Windows
req.typenames: PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, *PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
req.product: Windows 10 or later.
f1_keywords:
 - _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
 - wdm/_PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
 - PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
 - wdm/PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
 - PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
 - wdm/PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
 - PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
 - PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
---

# _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure (wdm.h)


## -description

The PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure describes a PCI Express (PCIe) uncorrectable error severity register of a PCIe advanced error reporting capability structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field AsULONG

A ULONG representation of the contents of the PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure.


### -field CompleterAbort

A single bit that indicates that a reported completer abort is a fatal error.


### -field CompletionTimeout

A single bit that indicates that a reported completion timeout is a fatal error.


### -field DataLinkProtocolError

A single bit that indicates that a reported data link protocol error is a fatal error.


### -field ECRCError

A single bit that indicates that a reported end-to-end cyclic redundancy check (ECRC) error is a fatal error.


### -field FlowControlProtocolError

A single bit that indicates that a reported flow control protocol error is a fatal error.


### -field MalformedTLP

A single bit that indicates that a reported malformed transaction layer packet (TLP) is a fatal error.


### -field PoisonedTLP

A single bit that indicates that a reported poisoned transaction layer packet (TLP) is a fatal error.


### -field ReceiverOverflow

A single bit that indicates that a reported receiver overflow is a fatal error.


### -field Reserved1

Reserved.


### -field Reserved2

Reserved.


### -field Reserved3

Reserved.


### -field SurpriseDownError

A single bit that indicates that a reported surprise down error is a fatal error.


### -field Undefined

A single bit that contains an undefined value. In versions of the <i>PCIe Specification</i> prior to version 1.1, this bit indicates that a reported link training error is a fatal error.


### -field UnexpectedCompletion

A single bit that indicates that a reported unexpected completion is a fatal error.


### -field UnsupportedRequestError

A single bit that indicates that a reported unsupported request error is a fatal error.

## -syntax

```cpp
typedef union _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY {
  struct {
    ULONG Undefined  :1;
    ULONG Reserved1  :3;
    ULONG DataLinkProtocolError  :1;
    ULONG SurpriseDownError  :1;
    ULONG Reserved2  :6;
    ULONG PoisonedTLP  :1;
    ULONG FlowControlProtocolError  :1;
    ULONG CompletionTimeout  :1;
    ULONG CompleterAbort  :1;
    ULONG UnexpectedCompletion  :1;
    ULONG ReceiverOverflow  :1;
    ULONG MalformedTLP  :1;
    ULONG ECRCError  :1;
    ULONG UnsupportedRequestError  :1;
    ULONG Reserved3  :11;
  };
  ULONG  AsULONG;
} PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, *PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY;
```

## -remarks

The PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure is contained in the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_aer_capability">PCI_EXPRESS_AER_CAPABILITY</a>, <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_bridge_aer_capability">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>, and <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_rootport_aer_capability">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a> structures.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_aer_capability">PCI_EXPRESS_AER_CAPABILITY</a>



<a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_bridge_aer_capability">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>



<a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_rootport_aer_capability">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a>

