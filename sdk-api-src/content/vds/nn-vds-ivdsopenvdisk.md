---
UID: NN:vds.IVdsOpenVDisk
title: IVdsOpenVDisk (vds.h)
description: Defines methods for managing a virtual disk.
helpviewer_keywords: ["IVdsOpenVDisk","IVdsOpenVDisk interface","IVdsOpenVDisk interface","described","base.ivdsopenvdisk","vds/IVdsOpenVDisk"]
old-location: base\ivdsopenvdisk.htm
tech.root: VDS
ms.assetid: 3d5f080f-3e83-437e-8cbc-9730988f5dcc
ms.date: 12/05/2018
ms.keywords: IVdsOpenVDisk, IVdsOpenVDisk interface, IVdsOpenVDisk interface,described, base.ivdsopenvdisk, vds/IVdsOpenVDisk
f1_keywords:
- vds/IVdsOpenVDisk
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsOpenVDisk
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsOpenVDisk interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines methods for managing a virtual disk.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsOpenVDisk</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsOpenVDisk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsOpenVDisk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsopenvdisk-attach">Attach</a>
</td>
<td align="left" width="63%">
Attaches a virtual disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsopenvdisk-compact">Compact</a>
</td>
<td align="left" width="63%">
Compacts the virtual disk to reduce the physical size of the backing file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsopenvdisk-detach">Detach</a>
</td>
<td align="left" width="63%">
Detaches a virtual disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsopenvdisk-detachanddelete">DetachAndDelete</a>
</td>
<td align="left" width="63%">
Detaches a virtual disk and deletes the backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsopenvdisk-expand">Expand</a>
</td>
<td align="left" width="63%">
Increases the size of a virtual disk to the maximum size available on a fixed or expandable disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsopenvdisk-merge">Merge</a>
</td>
<td align="left" width="63%">
Merges a child virtual disk with its parents in the differencing chain.

</td>
</tr>
</table> 

