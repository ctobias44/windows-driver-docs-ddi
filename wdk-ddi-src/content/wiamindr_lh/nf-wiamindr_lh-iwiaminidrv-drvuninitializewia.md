---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvUnInitializeWia
title: IWiaMiniDrv::drvUnInitializeWia (wiamindr_lh.h)
description: The IWiaMiniDrv::drvUnInitializeWia method releases resources held by the minidriver.
old-location: image\iwiaminidrv_drvuninitializewia.htm
tech.root: image
ms.date: 05/03/2018
keywords: ["IWiaMiniDrv::drvUnInitializeWia"]
ms.keywords: IWiaMiniDrv interface [Imaging Devices],drvUnInitializeWia method, IWiaMiniDrv.drvUnInitializeWia, IWiaMiniDrv::drvUnInitializeWia, MiniDrv_2a06b98b-7b47-46d8-b158-8e6ff6bac6b9.xml, drvUnInitializeWia, drvUnInitializeWia method [Imaging Devices], drvUnInitializeWia method [Imaging Devices],IWiaMiniDrv interface, image.iwiaminidrv_drvuninitializewia, wiamindr_lh/IWiaMiniDrv::drvUnInitializeWia
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Desktop
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
req.typenames: 
f1_keywords:
 - IWiaMiniDrv::drvUnInitializeWia
 - wiamindr_lh/IWiaMiniDrv::drvUnInitializeWia
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wiamindr_lh.h
api_name:
 - IWiaMiniDrv::drvUnInitializeWia
---

# IWiaMiniDrv::drvUnInitializeWia


## -description

The **IWiaMiniDrv::drvUnInitializeWia** method releases resources held by the minidriver.

## -parameters

### -param __MIDL__IWiaMiniDrv0064

pWiasContext [in]

- Pointer to a WIA item context.

### -param pWiasContext [in]

Pointer to a WIA item context.

## -returns

On success, the method should return S_OK If the method fails, it should return a standard COM error code.

## -remarks

The WIA service calls the **IWiaMiniDrv::drvUnInitializeWia** method when the resources associated with an application item tree are no longer needed. The minidriver can then unload any DLLs and free any allocated memory.

## -see-also

[IWiaMiniDrv](./nn-wiamindr_lh-iwiaminidrv.md)

[IWiaMiniDrv::drvInitializeWia](./nf-wiamindr_lh-iwiaminidrv-drvinitializewia.md)

