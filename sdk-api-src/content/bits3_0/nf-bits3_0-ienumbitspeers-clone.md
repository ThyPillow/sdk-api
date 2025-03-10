---
UID: NF:bits3_0.IEnumBitsPeers.Clone
title: IEnumBitsPeers::Clone (bits3_0.h)
description: Creates another IEnumBitsPeers enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [BITS]","Clone method [BITS]","IEnumBitsPeers interface","IEnumBitsPeers interface [BITS]","Clone method","IEnumBitsPeers.Clone","IEnumBitsPeers::Clone","bits.ienumbitspeers_clone","bits3_0/IEnumBitsPeers::Clone"]
old-location: bits\ienumbitspeers_clone.htm
tech.root: Bits
ms.assetid: 72b3e0bc-9426-4953-a910-2dfaa955c4c0
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBitsPeers interface, IEnumBitsPeers interface [BITS],Clone method, IEnumBitsPeers.Clone, IEnumBitsPeers::Clone, bits.ienumbitspeers_clone, bits3_0/IEnumBitsPeers::Clone
f1_keywords:
- bits3_0/IEnumBitsPeers.Clone
dev_langs:
- c++
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Bits.lib
- Bits.dll
api_name:
- IEnumBitsPeers.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumBitsPeers::Clone


## -description


Creates another 
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeers">IEnumBitsPeers</a> enumerator that contains the same enumeration state as the current one.

Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.


## -parameters




### -param ppenum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppEnum</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nn-bits3_0-ienumbitspeers">IEnumBitsPeers</a>
 

 

