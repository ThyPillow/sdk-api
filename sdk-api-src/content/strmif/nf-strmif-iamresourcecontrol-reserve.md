---
UID: NF:strmif.IAMResourceControl.Reserve
title: IAMResourceControl::Reserve (strmif.h)
description: The Reserve method reserves or unreserves a device resource.
helpviewer_keywords: ["IAMResourceControl interface [DirectShow]","Reserve method","IAMResourceControl.Reserve","IAMResourceControl::Reserve","IAMResourceControlReserve","Reserve","Reserve method [DirectShow]","Reserve method [DirectShow]","IAMResourceControl interface","dshow.iamresourcecontrol_reserve","strmif/IAMResourceControl::Reserve"]
old-location: dshow\iamresourcecontrol_reserve.htm
tech.root: DirectShow
ms.assetid: 5f264b87-dae4-4478-811f-1c99e670928a
ms.date: 12/05/2018
ms.keywords: IAMResourceControl interface [DirectShow],Reserve method, IAMResourceControl.Reserve, IAMResourceControl::Reserve, IAMResourceControlReserve, Reserve, Reserve method [DirectShow], Reserve method [DirectShow],IAMResourceControl interface, dshow.iamresourcecontrol_reserve, strmif/IAMResourceControl::Reserve
f1_keywords:
- strmif/IAMResourceControl.Reserve
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMResourceControl.Reserve
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMResourceControl::Reserve


## -description



The <code>Reserve</code> method reserves or unreserves a device resource.




## -parameters




### -param dwFlags [in]

Flag indicating whether to reserve or unreserve this device. The value must be a member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_amresctl_reserveflags">AMRESCTL_RESERVEFLAGS</a> enumeration.


### -param pvReserved [in]

Must be <b>NULL</b>.


## -returns



Returns S_OK if the device was successfully reserved or unreserved, S_FALSE if the device is currently reserved and will continue to be held, or an <b>HRESULT</b> error code if the device can't be reserved.




## -remarks



A resource can be reserved multiple times. If the method returns S_OK, the filter increments an internal reserve count. For every call to reserve a device that returns S_OK, the caller must make a matching call to unreserve the device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamresourcecontrol">IAMResourceControl Interface</a>
 

 

