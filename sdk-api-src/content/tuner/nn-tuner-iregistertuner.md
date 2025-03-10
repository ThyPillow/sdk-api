---
UID: NN:tuner.IRegisterTuner
title: IRegisterTuner (tuner.h)
description: This feature is expected to be available on a future version of the Windows operating system.
helpviewer_keywords: ["IRegisterTuner","IRegisterTuner interface [Microsoft TV Technologies]","IRegisterTuner interface [Microsoft TV Technologies]","described","IRegisterTunerInterface","mstv.iregistertuner","tuner/IRegisterTuner"]
old-location: mstv\iregistertuner.htm
tech.root: mstv
ms.assetid: 99e88361-f5d3-43b7-b879-2e1c44859af4
ms.date: 12/05/2018
ms.keywords: IRegisterTuner, IRegisterTuner interface [Microsoft TV Technologies], IRegisterTuner interface [Microsoft TV Technologies],described, IRegisterTunerInterface, mstv.iregistertuner, tuner/IRegisterTuner
f1_keywords:
- tuner/IRegisterTuner
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
- tuner.h
api_name:
- IRegisterTuner
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRegisterTuner interface


## -description



This feature is expected to be available on a future version of the Windows operating system.
        

The <b>IRegisterTuner</b> interface registers an apartment-threaded tuner with the tuner marshaller and registers the tuner marshaller with the graph service provider.

A common scenario that uses the video control involves a physical remote control sending infrared commands to a set-top box. The set-top box can be plugged into an auxiliary input or into the radio frequency (RF) tuner on the playback device. The analog tuner in the video control must be tuned to the input channel to receive the signal, but the content is actually on a different channel. Some filters need the actual content channel; they query <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner</a> to retrieve it.

However, an object outside the filter graph and the video control may be doing the actual tuning. If the external object is apartment-model threaded, synchronization issues may occur because <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner</a> can be called on any thread. The tuner marshaller is a utility object that simplifies this situation by storing the apartment model interface pointer and registering itself instead. Whenever the tuner marshaller <b>ITuner</b> interface is called, the tuner marshaller does the correct marshalling and passes the call to the external apartment-model object. The tuner marshaller also handles registering with the graph service provider.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRegisterTuner</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRegisterTuner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRegisterTuner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iregistertuner-register">Register</a>
</td>
<td align="left" width="63%">
Registers an apartment-threaded tuner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iregistertuner-unregister">Unregister</a>
</td>
<td align="left" width="63%">
Unregisters an apartment-threaded tuner.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IRegisterTuner)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

