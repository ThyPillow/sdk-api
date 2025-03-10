---
UID: NF:d3d10.ID3D10Device.IASetInputLayout
title: ID3D10Device::IASetInputLayout (d3d10.h)
description: Bind an input-layout object to the input-assembler stage.
helpviewer_keywords: ["5492ac19-1f40-6d42-38a5-490e297331f0","IASetInputLayout","IASetInputLayout method [Direct3D 10]","IASetInputLayout method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","IASetInputLayout method","ID3D10Device.IASetInputLayout","ID3D10Device::IASetInputLayout","d3d10/ID3D10Device::IASetInputLayout","direct3d10.id3d10device_iasetinputlayout"]
old-location: direct3d10\id3d10device_iasetinputlayout.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iasetinputlayout.htm
ms.date: 12/05/2018
ms.keywords: 5492ac19-1f40-6d42-38a5-490e297331f0, IASetInputLayout, IASetInputLayout method [Direct3D 10], IASetInputLayout method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IASetInputLayout method, ID3D10Device.IASetInputLayout, ID3D10Device::IASetInputLayout, d3d10/ID3D10Device::IASetInputLayout, direct3d10.id3d10device_iasetinputlayout
f1_keywords:
- d3d10/ID3D10Device.IASetInputLayout
dev_langs:
- c++
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D10.lib
- D3D10.dll
api_name:
- ID3D10Device.IASetInputLayout
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::IASetInputLayout


## -description


Bind an input-layout object to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.


## -parameters




### -param pInputLayout [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10inputlayout">ID3D10InputLayout</a>*</b>

A pointer to the input-layout object (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10inputlayout">ID3D10InputLayout</a>), which describes the input buffers that will be read by the IA stage.


## -remarks



Input-layout objects describe how vertex buffer data is streamed into the IA pipeline stage. To create an input-layout object, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createinputlayout">ID3D10Device::CreateInputLayout</a>.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

