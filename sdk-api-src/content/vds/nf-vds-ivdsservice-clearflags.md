---
UID: NF:vds.IVdsService.ClearFlags
title: IVdsService::ClearFlags (vds.h)
description: Clears service object flags.
helpviewer_keywords: ["ClearFlags","ClearFlags method [VDS]","ClearFlags method [VDS]","IVdsService interface","IVdsService interface [VDS]","ClearFlags method","IVdsService.ClearFlags","IVdsService::ClearFlags","base.ivdsservice_clearflags","vds/IVdsService::ClearFlags"]
old-location: base\ivdsservice_clearflags.htm
tech.root: VDS
ms.assetid: 91cb21ea-725b-4032-9a60-34c1b42b55d0
ms.date: 12/05/2018
ms.keywords: ClearFlags, ClearFlags method [VDS], ClearFlags method [VDS],IVdsService interface, IVdsService interface [VDS],ClearFlags method, IVdsService.ClearFlags, IVdsService::ClearFlags, base.ivdsservice_clearflags, vds/IVdsService::ClearFlags
f1_keywords:
- vds/IVdsService.ClearFlags
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- IVdsService.ClearFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsService::ClearFlags


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Clears service object flags.


## -parameters




### -param ulFlags [in]

The flags enumerated by <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-vds_service_flag">VDS_SERVICE_FLAG</a>. Callers can clear the <b>VDS_SVF_AUTO_MOUNT_OFF</b> flag.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The flags were cleared successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the service finishes initializing, the method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>
 




## -remarks



Beginning with Windows 8 and Windows Server 2012, the <b>VDS_SVF_AUTO_MOUNT_OFF</b> is deprecated. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-vds_san_policy">VDS_SAN_POLICY</a> enumeration to control default disk mounting behavior.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-vds_service_flag">VDS_SERVICE_FLAG</a>
 

 

