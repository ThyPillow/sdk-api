---
UID: NF:dwrite_3.IDWriteFontSet1.GetFilteredFonts(UINT32 const,UINT32,IDWriteFontSet1)
title: IDWriteFontSet1::GetFilteredFonts
description: Retrieves a subset of fonts, filtered by the given indices.
helpviewer_keywords: ["IDWriteFontSet1 interface [Direct Write]","GetFilteredFonts method","IDWriteFontSet1.GetFilteredFonts","IDWriteFontSet1::GetFilteredFonts","GetFilteredFonts","GetFilteredFonts method [Direct Write]","GetFilteredFonts method [Direct Write]","IDWriteFontSet1 interface","directwrite.idwritefontset1_getfilteredfonts","dwrite_3/IDWriteFontSet1::GetFilteredFonts"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet1 interface [Direct Write],GetFilteredFonts method, IDWriteFontSet1.GetFilteredFonts, IDWriteFontSet1::GetFilteredFonts, GetFilteredFonts, GetFilteredFonts method [Direct Write], GetFilteredFonts method [Direct Write],IDWriteFontSet1 interface, directwrite.idwritefontset1_getfilteredfonts, dwrite_3/IDWriteFontSet1::GetFilteredFonts
f1_keywords:
- dwrite_3/IDWriteFontSet1.GetFilteredFonts
dev_langs:
- c++
req.construct-type: function
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dwrite.lib
- Dwrite.dll
api_name:
- IDWriteFontSet1::GetFilteredFonts
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves a subset of fonts, filtered by the given indices.

## -parameters

### -param indices

Type: **[UINT32](/windows/win32/winprog/windows-data-types) const \***

An array of indices to filter by, in the range 0 to [IDwriteFontSet::GetFontCount](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getfontcount) minus 1.

### -param indexCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of indices.

### -param filteredFontSet [out]

Type: **[IDWriteFontSet1](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1)\*\***

The address of a pointer to an [IDWriteFontSet1](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) interface. On successful completion, the function sets the pointer to an object representing the subset of fonts indicated by the given indices, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

The indices can come in any order, meaning that **GetFilteredFonts** can produce a new set with items removed, duplicated, or reordered from the original. If you pass zero indices, then an empty font set is returned.

## -see-also
