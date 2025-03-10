---
UID: NF:strmif.IAMCertifiedOutputProtection.SessionSequenceStart
title: IAMCertifiedOutputProtection::SessionSequenceStart (strmif.h)
description: The SessionSequenceStart method initiates the COPP session with the graphics driver.
helpviewer_keywords: ["IAMCertifiedOutputProtection interface [DirectShow]","SessionSequenceStart method","IAMCertifiedOutputProtection.SessionSequenceStart","IAMCertifiedOutputProtection::SessionSequenceStart","IAMCertifiedOutputProtectionSessionSequenceStart","SessionSequenceStart","SessionSequenceStart method [DirectShow]","SessionSequenceStart method [DirectShow]","IAMCertifiedOutputProtection interface","dshow.iamcertifiedoutputprotection_sessionsequencestart","strmif/IAMCertifiedOutputProtection::SessionSequenceStart"]
old-location: dshow\iamcertifiedoutputprotection_sessionsequencestart.htm
tech.root: DirectShow
ms.assetid: 0321e315-b53c-487f-a015-80f7ed581737
ms.date: 12/05/2018
ms.keywords: IAMCertifiedOutputProtection interface [DirectShow],SessionSequenceStart method, IAMCertifiedOutputProtection.SessionSequenceStart, IAMCertifiedOutputProtection::SessionSequenceStart, IAMCertifiedOutputProtectionSessionSequenceStart, SessionSequenceStart, SessionSequenceStart method [DirectShow], SessionSequenceStart method [DirectShow],IAMCertifiedOutputProtection interface, dshow.iamcertifiedoutputprotection_sessionsequencestart, strmif/IAMCertifiedOutputProtection::SessionSequenceStart
f1_keywords:
- strmif/IAMCertifiedOutputProtection.SessionSequenceStart
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
- IAMCertifiedOutputProtection.SessionSequenceStart
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMCertifiedOutputProtection::SessionSequenceStart


## -description


The <code>SessionSequenceStart</code> method initiates the COPP session with the graphics driver.


## -parameters




### -param pSig [in]

Pointer to an [AMCOPPSignature](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-amcoppsignature) structure. Fill this structure as described in the Remarks session.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Invalid state. Possibly the application passed unexpected data, or called <b>IAMCertifiedOutputProtection</b> methods in the wrong order.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_COPP_HW</b></dt>
</dl>
</td>
<td width="60%">
The display device does not support COPP; or the VMR has not connected to a display device yet.

</td>
</tr>
</table>
 




## -remarks



To fill in the structure for the <i>pSig</i> parameter, first concatenate the following numbers:

<ul>
<li>The 128-bit number returned in the <i>pRandom</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange">IAMCertifiedOutputProtection::KeyExchange</a> method.</li>
<li>Data integrity session key. This value is a 128-bit random number generated by the application.</li>
<li>Starting sequence number for COPP status requests. This value is a 32-bit random number generated by the application.</li>
<li>Starting sequence number for COPP commands. This value is a 32-bit random number generated by the application.</li>
</ul>
Then encrypt this number with 2048-bit RSA encryption using the graphics driver's public encryption key. The public encryption key is contained in the certificate returned in the <i>VarLenCertGH</i> parameter of the <b>KeyExchange</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamcertifiedoutputprotection">IAMCertifiedOutputProtection Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>
 

 

