---
UID: NF:gdiplusheaders.FontFamily.FontFamily(IN const WCHAR,IN const FontCollection)
title: FontFamily::FontFamily(IN const WCHAR,IN const FontCollection) (gdiplusheaders.h)
description: Creates a FontFamily::FontFamily object based on a specified font family.
helpviewer_keywords: ["FontFamily","FontFamily class [GDI+]","FontFamily constructor","FontFamily constructor [GDI+]","FontFamily constructor [GDI+]","FontFamily class","FontFamily.FontFamily","FontFamily.FontFamily(IN const WCHAR","IN const FontCollection)","FontFamily.FontFamily(const WCHAR*","const FontCollection*)","FontFamily::FontFamily","FontFamily::FontFamily(IN const WCHAR","IN const FontCollection)","_gdiplus_CLASS_FontFamily_FontFamily_name_fontCollection_","gdiplus._gdiplus_CLASS_FontFamily_FontFamily_name_fontCollection_"]
old-location: gdiplus\_gdiplus_CLASS_FontFamily_FontFamily_name_fontCollection_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilyconstructors\fontfamily_44name_fontcollection.htm
ms.date: 12/05/2018
ms.keywords: FontFamily, FontFamily class [GDI+],FontFamily constructor, FontFamily constructor [GDI+], FontFamily constructor [GDI+],FontFamily class, FontFamily.FontFamily, FontFamily.FontFamily(IN const WCHAR,IN const FontCollection), FontFamily.FontFamily(const WCHAR*,const FontCollection*), FontFamily::FontFamily, FontFamily::FontFamily(IN const WCHAR,IN const FontCollection), _gdiplus_CLASS_FontFamily_FontFamily_name_fontCollection_, gdiplus._gdiplus_CLASS_FontFamily_FontFamily_name_fontCollection_
f1_keywords:
- gdiplusheaders/FontFamily.FontFamily
dev_langs:
- c++
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- FontFamily.FontFamily
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# FontFamily::FontFamily(IN const WCHAR,IN const FontCollection)


## -description


Creates a <b>FontFamily::FontFamily</b> object based on a specified font family.


## -parameters




### -param name [in]

Type: <b>const WCHAR*</b>

Name of the font family. For example, Arial.ttf is the name of the Arial font family. 


### -param fontCollection [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a>*</b>

Optional. Pointer to a 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a> object that specifies the collection that the font family belongs to. If 
					<b>FontCollection</b> is <b>NULL</b>, this font family is not part of a collection. The default value is <b>NULL</b>. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection">InstalledFontCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>
 

 

