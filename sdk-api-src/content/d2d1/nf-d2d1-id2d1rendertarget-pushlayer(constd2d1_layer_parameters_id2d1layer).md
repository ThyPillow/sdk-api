---
UID: NF:d2d1.ID2D1RenderTarget.PushLayer(const D2D1_LAYER_PARAMETERS,ID2D1Layer)
title: ID2D1RenderTarget::PushLayer (d2d1.h)
description: Adds the specified layer to the render target so that it receives all subsequent drawing operations until PopLayer is called.
helpviewer_keywords: ["ID2D1RenderTarget interface [Direct2D]","PushLayer method","ID2D1RenderTarget.PushLayer","ID2D1RenderTarget::PushLayer","ID2D1RenderTarget::PushLayer(const D2D1_LAYER_PARAMETERS","ID2D1Layer)","PushLayer","PushLayer method [Direct2D]","PushLayer method [Direct2D]","ID2D1RenderTarget interface","d2d1/ID2D1RenderTarget::PushLayer","direct2d.ID2D1RenderTarget_PushLayer_ptr_D2D1_LAYER_PARAMETERS_ptr_ID2D1Layer"]
old-location: direct2d\ID2D1RenderTarget_PushLayer_ptr_D2D1_LAYER_PARAMETERS_ptr_ID2D1Layer.htm
tech.root: Direct2D
ms.assetid: 0fc7ac38-ff74-4f3b-9aa2-025a99e6b013
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],PushLayer method, ID2D1RenderTarget.PushLayer, ID2D1RenderTarget::PushLayer, ID2D1RenderTarget::PushLayer(const D2D1_LAYER_PARAMETERS,ID2D1Layer), PushLayer, PushLayer method [Direct2D], PushLayer method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::PushLayer, direct2d.ID2D1RenderTarget_PushLayer_ptr_D2D1_LAYER_PARAMETERS_ptr_ID2D1Layer
f1_keywords:
- d2d1/ID2D1RenderTarget.PushLayer
dev_langs:
- c++
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
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
- ID2D1RenderTarget.PushLayer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::PushLayer


## -description


Adds the specified layer to the render target so that it receives all subsequent drawing operations until <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a> is called. 


## -parameters




### -param layerParameters [in]

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_layer_parameters">D2D1_LAYER_PARAMETERS</a>*</b>

The content bounds, geometric mask, opacity, opacity mask, and antialiasing options for the layer. 


### -param layer [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1layer">ID2D1Layer</a>*</b>

The layer that receives subsequent drawing operations.

<div class="alert"><b>Note</b>  Starting with Windows 8, this parameter is optional. If a layer is not specified, Direct2D manages the layer resource automatically.</div>
<div> </div>

## -remarks



The <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)">PushLayer</a> method allows a caller to begin redirecting rendering to a layer. All rendering operations are valid in a layer. The location of the layer is affected by the world transform set on the render target. 

Each <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)">PushLayer</a> must have a matching <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a> call. If there are more <b>PopLayer</b> calls than <b>PushLayer</b> calls, the render target is placed into an error state. If <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">Flush</a> is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned. The error state can be cleared by a call to <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a>.

A particular <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)">ID2D1Layer</a> resource can be active only at one time. In other words, you cannot call a <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> method, and then  immediately follow with another <b>PushLayer</b> method with the same layer resource. Instead, you must call the second <b>PushLayer</b> method with different layer resources. 


This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)">PushLayer</a>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/win32/Direct2D/direct2d-layers-overview">Layers Overview</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a>
 

 

