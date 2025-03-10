---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateInk(const D2D1_INK_POINT,ID2D1Ink)
title: ID2D1DeviceContext2::CreateInk(const D2D1_INK_POINT,ID2D1Ink) (d2d1_3.h)
description: Creates a new ID2D1Ink object that starts at the given point.
helpviewer_keywords: ["CreateInk","CreateInk method [Direct2D]","CreateInk method [Direct2D]","ID2D1DeviceContext2 interface","ID2D1DeviceContext2 interface [Direct2D]","CreateInk method","ID2D1DeviceContext2.CreateInk","ID2D1DeviceContext2.CreateInk(const D2D1_INK_POINT","ID2D1Ink)","ID2D1DeviceContext2::CreateInk","ID2D1DeviceContext2::CreateInk(const D2D1_INK_POINT","ID2D1Ink)","d2d1_3/ID2D1DeviceContext2::CreateInk","direct2d.id2d1devicecontext2_createink2"]
old-location: direct2d\id2d1devicecontext2_createink2.htm
tech.root: Direct2D
ms.assetid: c98ecb40-1039-a9fa-9596-0d42719a1cc7
ms.date: 12/05/2018
ms.keywords: CreateInk, CreateInk method [Direct2D], CreateInk method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateInk method, ID2D1DeviceContext2.CreateInk, ID2D1DeviceContext2.CreateInk(const D2D1_INK_POINT,ID2D1Ink), ID2D1DeviceContext2::CreateInk, ID2D1DeviceContext2::CreateInk(const D2D1_INK_POINT,ID2D1Ink), d2d1_3/ID2D1DeviceContext2::CreateInk, direct2d.id2d1devicecontext2_createink2
f1_keywords:
- d2d1_3/ID2D1DeviceContext2.CreateInk
dev_langs:
- c++
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1DeviceContext2.CreateInk
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext2::CreateInk(const D2D1_INK_POINT,ID2D1Ink)


## -description


Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a> object that starts at the given point.


## -parameters




### -param startPoint

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point">D2D1_INK_POINT</a>*</b>

The starting point of the first segment of the first stroke in the new ink object.


### -param ink [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a>**</b>

When this method returns, contains the address of a pointer to a new ink object.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>
 

 

