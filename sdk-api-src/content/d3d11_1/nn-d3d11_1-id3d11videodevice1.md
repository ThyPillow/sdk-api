---
UID: NN:d3d11_1.ID3D11VideoDevice1
title: ID3D11VideoDevice1 (d3d11_1.h)
description: Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device.
helpviewer_keywords: ["ID3D11VideoDevice1","ID3D11VideoDevice1 interface [Media Foundation]","ID3D11VideoDevice1 interface [Media Foundation]","described","d3d11_1/ID3D11VideoDevice1","mf.id3d11videodevice1"]
old-location: mf\id3d11videodevice1.htm
tech.root: medfound
ms.assetid: 10E68945-6103-491D-8846-3B7C880FEAFD
ms.date: 12/05/2018
ms.keywords: ID3D11VideoDevice1, ID3D11VideoDevice1 interface [Media Foundation], ID3D11VideoDevice1 interface [Media Foundation],described, d3d11_1/ID3D11VideoDevice1, mf.id3d11videodevice1
f1_keywords:
- d3d11_1/ID3D11VideoDevice1
dev_langs:
- c++
req.header: d3d11_1.h
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d11_1.h
api_name:
- ID3D11VideoDevice1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoDevice1 interface


## -description


Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoDevice1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>. <b>ID3D11VideoDevice1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoDevice1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-checkvideodecoderdownsampling">CheckVideoDecoderDownsampling</a>
</td>
<td align="left" width="63%">
Indicates whether the video decoder supports downsampling with the specified input format, and whether real-time downsampling is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getcryptosessionprivatedatasize">GetCryptoSessionPrivateDataSize</a>
</td>
<td align="left" width="63%">
Retrieves optional sizes for private driver data. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getvideodecodercaps">GetVideoDecoderCaps</a>
</td>
<td align="left" width="63%">
Retrieves capabilities and limitations of the video decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-recommendvideodecoderdownsampleparameters">RecommendVideoDecoderDownsampleParameters</a>
</td>
<td align="left" width="63%">
Allows the driver to recommend optimal output downsample parameters from the input parameters.

</td>
</tr>
</table> 


## -remarks



The Direct3D 11 device supports this interface. To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a> interface pointer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>
 

 

