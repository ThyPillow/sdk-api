---
UID: NF:d2d1_1.ID2D1DeviceContext.FillOpacityMask(ID2D1Bitmap,ID2D1Brush,const D2D1_RECT_F,const D2D1_RECT_F)
title: ID2D1DeviceContext::FillOpacityMask (d2d1_1.h)
description: Fill using the alpha channel of the supplied opacity mask bitmap. The brush opacity will be modulated by the mask. The render target antialiasing mode must be set to aliased.
helpviewer_keywords: ["FillOpacityMask","FillOpacityMask method [Direct2D]","FillOpacityMask method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","FillOpacityMask method","ID2D1DeviceContext.FillOpacityMask","ID2D1DeviceContext::FillOpacityMask","ID2D1DeviceContext::FillOpacityMask(ID2D1Bitmap","ID2D1Brush","const D2D1_RECT_F","const D2D1_RECT_F)","d2d1_1/ID2D1DeviceContext::FillOpacityMask","direct2d.id2d1devicecontext_fillopacitymask"]
old-location: direct2d\id2d1devicecontext_fillopacitymask.htm
tech.root: Direct2D
ms.assetid: 5D5BF7E9-AC5A-49B7-A04E-97B8377243FE
ms.date: 12/05/2018
ms.keywords: FillOpacityMask, FillOpacityMask method [Direct2D], FillOpacityMask method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],FillOpacityMask method, ID2D1DeviceContext.FillOpacityMask, ID2D1DeviceContext::FillOpacityMask, ID2D1DeviceContext::FillOpacityMask(ID2D1Bitmap,ID2D1Brush,const D2D1_RECT_F,const D2D1_RECT_F), d2d1_1/ID2D1DeviceContext::FillOpacityMask, direct2d.id2d1devicecontext_fillopacitymask
f1_keywords:
- d2d1_1/ID2D1DeviceContext.FillOpacityMask
dev_langs:
- c++
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
- ID2D1DeviceContext.FillOpacityMask
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext::FillOpacityMask


## -description


Fill using the alpha channel of the supplied opacity mask bitmap. The brush opacity will be modulated by the mask. The render target antialiasing mode must be set to aliased.


## -parameters




### -param opacityMask [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap that acts as the opacity mask


### -param brush [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush to use for filling the primitive.


### -param destinationRectangle [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The destination rectangle to output to in the render target


### -param sourceRectangle [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The source rectangle from the opacity mask bitmap.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>
 

 

