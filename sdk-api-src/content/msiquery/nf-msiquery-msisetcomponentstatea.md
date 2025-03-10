---
UID: NF:msiquery.MsiSetComponentStateA
title: MsiSetComponentStateA function (msiquery.h)
description: The MsiSetComponentState function sets a component to the requested state.
helpviewer_keywords: ["INSTALLSTATE_ABSENT","INSTALLSTATE_LOCAL","INSTALLSTATE_SOURCE","MsiSetComponentState","MsiSetComponentState function","MsiSetComponentStateA","MsiSetComponentStateW","_msi_msisetcomponentstate","msiquery/MsiSetComponentState","msiquery/MsiSetComponentStateA","msiquery/MsiSetComponentStateW","setup.msisetcomponentstate"]
old-location: setup\msisetcomponentstate.htm
tech.root: Msi
ms.assetid: d538c81f-130b-4522-9f85-47f04e24f125
ms.date: 12/05/2018
ms.keywords: INSTALLSTATE_ABSENT, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MsiSetComponentState, MsiSetComponentState function, MsiSetComponentStateA, MsiSetComponentStateW, _msi_msisetcomponentstate, msiquery/MsiSetComponentState, msiquery/MsiSetComponentStateA, msiquery/MsiSetComponentStateW, setup.msisetcomponentstate
f1_keywords:
- msiquery/MsiSetComponentState
dev_langs:
- c++
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSetComponentStateW (Unicode) and MsiSetComponentStateA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Msi.dll
api_name:
- MsiSetComponentState
- MsiSetComponentStateA
- MsiSetComponentStateW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiSetComponentStateA function


## -description


The 
<b>MsiSetComponentState</b> function sets a component to the requested state.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.


### -param szComponent [in]

Specifies the name of the component.


### -param iState [in]

Specifies the state to set. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ABSENT"></a><a id="installstate_absent"></a><dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The component was uninstalled.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The component was installed on the local drive.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The component will run from source, CD, or network.

</td>
</tr>
</table>
 


## -returns



The 
<b>MsiSetComponentState</b> function returns the following values:
					




## -remarks



The 
<b>MsiSetComponentState</b> function requests a change in the Action state of a record in the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/component-table">Component table</a>.

For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions From Programs</a>.

If the function fails, you can obtain extended error information by using <a href="https://docs.microsoft.com/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiSetComponentState as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Installer Selection Functions</a>
 

 

