---
UID: NF:vds.IVdsHwProviderStoragePools.QueryMaxLunCreateSizeInStoragePool
title: IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool (vds.h)
description: Returns the maximum size of the LUN that can be created in the storage pool based on the specified LUN type and hints.
helpviewer_keywords: ["IVdsHwProviderStoragePools interface","QueryMaxLunCreateSizeInStoragePool method","IVdsHwProviderStoragePools.QueryMaxLunCreateSizeInStoragePool","IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool","QueryMaxLunCreateSizeInStoragePool","QueryMaxLunCreateSizeInStoragePool method","QueryMaxLunCreateSizeInStoragePool method","IVdsHwProviderStoragePools interface","base.ivdshwproviderstoragepools_querymaxluncreatesizeinstoragepool","vds/IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool","vdshwprv/IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool"]
old-location: base\ivdshwproviderstoragepools_querymaxluncreatesizeinstoragepool.htm
tech.root: VDS
ms.assetid: 37a802e2-4573-4f47-bf54-b2197034722d
ms.date: 12/05/2018
ms.keywords: IVdsHwProviderStoragePools interface,QueryMaxLunCreateSizeInStoragePool method, IVdsHwProviderStoragePools.QueryMaxLunCreateSizeInStoragePool, IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool, QueryMaxLunCreateSizeInStoragePool, QueryMaxLunCreateSizeInStoragePool method, QueryMaxLunCreateSizeInStoragePool method,IVdsHwProviderStoragePools interface, base.ivdshwproviderstoragepools_querymaxluncreatesizeinstoragepool, vds/IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool, vdshwprv/IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool
f1_keywords:
- vds/IVdsHwProviderStoragePools.QueryMaxLunCreateSizeInStoragePool
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
- IVdsHwProviderStoragePools.QueryMaxLunCreateSizeInStoragePool
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the maximum size of the LUN that can be created in the <a href="https://docs.microsoft.com/windows/desktop/VDS/storage-pool-object">storage pool</a> based on the specified LUN type and hints.


## -parameters




### -param type [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a> enumeration value that specifies the LUN type. This parameter is required and must be a valid LUN type.


### -param StoragePoolId [in]

A VDS_OBJECT_ID (GUID) value that identifies the storage pools to be used to create the new LUN. This parameter is required and cannot be GUID_NULL.


### -param pHints2 [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure that contains hints to be used in creating the LUN.


### -param pullMaxLunSize [out]

The address of a ULONGLONG value that receives the maximum LUN size, in bytes.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwproviderstoragepools">IVdsHwProviderStoragePools</a>
 

 

