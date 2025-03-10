---
UID: NF:provider.Provider.DeleteInstance(const CInstance &,long)
title: Provider::DeleteInstance (provider.h)
description: The DeleteInstance method is called by WMI to delete an instance.
helpviewer_keywords: ["DeleteInstance","DeleteInstance method [Windows Management Instrumentation]","DeleteInstance method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","DeleteInstance method","Provider.DeleteInstance","Provider::DeleteInstance","_hmm_provider_deleteinstance","provider/Provider::DeleteInstance","wmi.provider_deleteinstance"]
old-location: wmi\provider_deleteinstance.htm
tech.root: WmiSdk
ms.assetid: 469d2481-95ea-4d17-b0ef-095ced9c8319
ms.date: 12/05/2018
ms.keywords: DeleteInstance, DeleteInstance method [Windows Management Instrumentation], DeleteInstance method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],DeleteInstance method, Provider.DeleteInstance, Provider::DeleteInstance, _hmm_provider_deleteinstance, provider/Provider::DeleteInstance, wmi.provider_deleteinstance
f1_keywords:
- provider/Provider.DeleteInstance
dev_langs:
- c++
req.header: provider.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- Provider.DeleteInstance
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Provider::DeleteInstance


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/provider/nl-provider-provider">Provider</a> class is part of the WMI 
    Provider Framework which is now considered in final state, and no further development, enhancements, or updates 
    will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>DeleteInstance</b> method is called by WMI to delete an instance.


## -parameters




#### - newInstance [ref]

Instance to be deleted.


### -param lFlags

Bitmask of flags with information about the delete operation. This is the value specified by the client in the <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">IWbemServices::DeleteInstance</a> function.

The following flag is handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>

## -returns



The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling function. The <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">IWbemServices::DeleteInstance</a> function lists the most common return values, although you can choose to return any COM return code.




## -remarks



WMI invokes <b>DeleteInstance</b> when a client calls <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">IWbemServices::DeleteInstance</a> against a class. Therefore, you must implement <b>DeleteInstance</b> if your framework provider supports deleting instances. The following list describes a common implementation of <b>DeleteInstance</b>:

<ol>
<li>Determine which instance the client requested by reading the key properties with one of the <b>Get</b> methods for <a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a>, such as <a href="https://docs.microsoft.com/windows/desktop/api/instance/nf-instance-cinstance-getchstring">CInstance::GetCHString</a>.</li>
<li>Delete the instance.</li>
</ol>
For more information about deleting instances, see <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">IWbemServices::DeleteInstance</a>.



