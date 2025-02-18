---
UID: NF:wiamindr_lh.IWiaDrvItem.GetItemFlags
title: IWiaDrvItem::GetItemFlags (wiamindr_lh.h)
description: The IWiaDrvItem::GetItemFlags method gets the item flags of the current IWiaDrvItem item.
old-location: image\iwiadrvitem_getitemflags.htm
tech.root: image
ms.date: 05/03/2018
keywords: ["IWiaDrvItem::GetItemFlags"]
ms.keywords: DrvItem_6fcac1f5-c754-4158-a1a0-61efe0d3913c.xml, GetItemFlags, GetItemFlags method [Imaging Devices], GetItemFlags method [Imaging Devices],IWiaDrvItem interface, IWiaDrvItem interface [Imaging Devices],GetItemFlags method, IWiaDrvItem.GetItemFlags, IWiaDrvItem::GetItemFlags, image.iwiadrvitem_getitemflags, wiamindr_lh/IWiaDrvItem::GetItemFlags
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
 - IWiaDrvItem::GetItemFlags
 - wiamindr_lh/IWiaDrvItem::GetItemFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wiamindr_lh.h
api_name:
 - IWiaDrvItem::GetItemFlags
---

# IWiaDrvItem::GetItemFlags


## -description

The **IWiaDrvItem::GetItemFlags** method gets the item flags of the current **IWiaDrvItem** item.

## -parameters

plFlags [out]

- Points to a memory location that will receive the item flags.

### -param __MIDL__IWiaDrvItem0000

### -param plFlags [out]

Points to a memory location that will receive the item flags.

## -returns

If the method succeeds, it places the item flag values in the location pointed to by *plFlags* and returns S_OK. If the pointer *plFlags* is invalid, the method returns E_INVALIDARG. If the method fails for another reason, it returns a standard COM error code.

## -remarks

The method places the current **IWiaDrvItem** item's flag values in the location pointed to by *pIFlags*. The item's flag values were set when the item was created by the driver services library function [wiasCreateDrvItem](../wiamdef/nf-wiamdef-wiascreatedrvitem.md).

## -see-also

[IWiaDrvItem](./nn-wiamindr_lh-iwiadrvitem.md)

[wiasCreateDrvItem](../wiamdef/nf-wiamdef-wiascreatedrvitem.md)

