---
UID: NC:gdiplustypes.EnumerateMetafileProc
title: EnumerateMetafileProc
ms.date: 11/4/2019
ms.topic: language-reference
targetos: Windows
description: \**EnumerateMetafileProc** is the signature of a callback function that you implement in your application for the [**Graphics::EnumerateMetafile**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-enumeratemetafile(inconstmetafile_inconstpointf_inint_inconstrectf__inunit_inenumeratemetafileproc_invoid_inconstimageattributes)) method (and overloads).
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplustypes.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - gdiplustypes.h
api_name:
 - EnumerateMetafileProc
f1_keywords:
 - gdiplustypes/EnumerateMetafileProc
dev_langs:
 - c++
---

## -description

**EnumerateMetafileProc** is the signature of a callback function that you implement in your application for the [**Graphics::EnumerateMetafile**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-enumeratemetafile(inconstmetafile_inconstpointf_inint_inconstrectf__inunit_inenumeratemetafileproc_invoid_inconstimageattributes)) method (and overloads).

In turn, your implementation can call [**Metafile::PlayRecord**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-playrecord) to play the record that was just enumerated.

## -parameters

### -param Arg1

Type: **[EmfPlusRecordType](/windows/win32/api/gdiplusenums/ne-gdiplusenums-emfplusrecordtype)**

The WMF, EMF, or EMF+ record type.

### -param Arg2

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

Flags; always 0 for WMF/EMF records.

### -param Arg3

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

The size of the record data (in bytes), or 0 if no data.

### -param Arg4

Type: **[BYTE](/windows/win32/winprog/windows-data-types)***

A pointer to the record data, or **NULL** if no data.

### -param Arg5

Type: **[VOID](/windows/win32/winprog/windows-data-types)\***

A pointer to callbackData, if any.

## -returns

Return **FALSE** to abort the enumeration process; return **TRUE** to continue it.

## -remarks

## -see-also