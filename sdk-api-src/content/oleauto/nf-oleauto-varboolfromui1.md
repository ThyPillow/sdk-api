---
UID: NF:oleauto.VarBoolFromUI1
title: VarBoolFromUI1 function (oleauto.h)
description: Converts an unsigned char value to a Boolean value.
helpviewer_keywords: ["VarBoolFromUI1","VarBoolFromUI1 function [Automation]","_oa96_VarBoolFromUI1","automat.varboolfromui1","oleauto/VarBoolFromUI1"]
old-location: automat\varboolfromui1.htm
tech.root: automat
ms.assetid: 50f27808-ab41-4883-9c0f-abb04a0d2d34
ms.date: 12/05/2018
ms.keywords: VarBoolFromUI1, VarBoolFromUI1 function [Automation], _oa96_VarBoolFromUI1, automat.varboolfromui1, oleauto/VarBoolFromUI1
f1_keywords:
- oleauto/VarBoolFromUI1
dev_langs:
- c++
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- OleAut32.dll
api_name:
- VarBoolFromUI1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarBoolFromUI1 function


## -description


Converts an unsigned char value to a Boolean value.


## -parameters




### -param bIn [in]

The value to convert.


### -param pboolOut [out]

The resulting value.


## -returns



This function can return one of these values.

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
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
The input parameter is not a valid type of variant.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The data pointed to by the output parameter does not fit in the destination type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The argument could not be coerced to the specified type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 



