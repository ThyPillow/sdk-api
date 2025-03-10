---
UID: NF:wuapi.ICategory.get_Description
title: ICategory::get_Description (wuapi.h)
description: Gets the description of the category.
helpviewer_keywords: ["Description property [Windows Update Agent]","Description property [Windows Update Agent]","ICategory interface","ICategory interface [Windows Update Agent]","Description property","ICategory.Description","ICategory.get_Description","ICategory::Description","ICategory::get_Description","get_Description","wua.icategory_description","wuapi/ICategory::Description","wuapi/ICategory::get_Description"]
old-location: wua\icategory_description.htm
tech.root: Wua_Sdk
ms.assetid: ef22db9f-2ac8-4f20-b898-774dd9b1ce8f
ms.date: 12/05/2018
ms.keywords: Description property [Windows Update Agent], Description property [Windows Update Agent],ICategory interface, ICategory interface [Windows Update Agent],Description property, ICategory.Description, ICategory.get_Description, ICategory::Description, ICategory::get_Description, get_Description, wua.icategory_description, wuapi/ICategory::Description, wuapi/ICategory::get_Description
f1_keywords:
- wuapi/ICategory.Description
dev_langs:
- c++
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wuapi.dll
api_name:
- ICategory.Description
- ICategory.get_Description
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICategory::get_Description


## -description


Gets the description of the category.

This property is read-only.


## -parameters


## -remarks



A <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_categories">Categories</a> property exists for the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> interface. And, a <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry2-get_categories">Categories</a> property exists for the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry2">IUpdateHistoryEntry2</a> interface. Therefore, the information that is used by the localized properties of the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a> interface depends on the Windows Update Agent (WUA) object that owns the <b>ICategory</b> interface.

 If the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a> interface is returned from the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_categories">Categories</a> property of <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>, the <b>ICategory</b> interface follows the localization rules of the <b>IUpdate</b> interface. In this case, if the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface  is created by using the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the language that is specified by the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a> interface of the session that is used to create <b>IUpdateSearcher</b>.

If a language preference is not specified by the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a> interface, or if the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface is not  created by using the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, WUA uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that the provider of the  update recommends.

If the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a> interface is returned from the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry2-get_categories">Categories</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry2">IUpdateHistoryEntry2</a> interface, the <b>ICategory</b> interface follows the localization rules of the <b>IUpdateHistoryEntry2</b> interface. The information  that   this property returns is for the default UI language of the user. If the default UI language of the user is unavailable, WUA uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that the provider of the  update recommends.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a>
 

 

