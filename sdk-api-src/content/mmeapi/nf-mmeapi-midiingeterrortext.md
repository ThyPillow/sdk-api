---
UID: NF:mmeapi.midiInGetErrorText
title: midiInGetErrorText function (mmeapi.h)
description: The midiInGetErrorText function retrieves a textual description for an error identified by the specified error code.
helpviewer_keywords: ["_win32_midiInGetErrorText","midiInGetErrorText","midiInGetErrorText function [Windows Multimedia]","midiInGetErrorTextA","midiInGetErrorTextW","mmeapi/midiInGetErrorText","mmeapi/midiInGetErrorTextA","mmeapi/midiInGetErrorTextW","multimedia.midiingeterrortext"]
old-location: multimedia\midiingeterrortext.htm
tech.root: Multimedia
ms.assetid: 0e653d6d-4d34-45c0-8ec9-975b885a5ef8
ms.date: 12/05/2018
ms.keywords: _win32_midiInGetErrorText, midiInGetErrorText, midiInGetErrorText function [Windows Multimedia], midiInGetErrorTextA, midiInGetErrorTextW, mmeapi/midiInGetErrorText, mmeapi/midiInGetErrorTextA, mmeapi/midiInGetErrorTextW, multimedia.midiingeterrortext
f1_keywords:
- mmeapi/midiInGetErrorText
dev_langs:
- c++
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: midiInGetErrorTextW (Unicode) and midiInGetErrorTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Winmm.dll
- API-MS-Win-mm-mme-l1-1-0.dll
- winmmbase.dll
api_name:
- midiInGetErrorText
- midiInGetErrorTextA
- midiInGetErrorTextW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# midiInGetErrorText function


## -description



The <b>midiInGetErrorText</b> function retrieves a textual description for an error identified by the specified error code.




## -parameters




### -param mmrError

Error code.


### -param pszText

Pointer to the buffer to be filled with the textual error description.


### -param cchText

Length, in characters, of the buffer pointed to by <i>lpText</i>.


## -returns



Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADERRNUM</b></dt>
</dl>
</td>
<td width="60%">
The specified error number is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer or structure is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate or lock memory.

</td>
</tr>
</table>
 




## -remarks



If the textual error description is longer than the specified buffer, the description is truncated. The returned error string is always null-terminated. If <i>cchText</i> is zero, nothing is copied, and the function returns zero. All error descriptions are less than MAXERRORLENGTH characters long.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
 

 

