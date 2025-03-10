---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetIsSideways
title: IXpsOMGlyphsEditor::GetIsSideways (xpsobjectmodel.h)
description: Gets a Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.
helpviewer_keywords: ["FALSE","GetIsSideways","GetIsSideways method [XPS Documents and Packaging]","GetIsSideways method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","GetIsSideways method","IXpsOMGlyphsEditor.GetIsSideways","IXpsOMGlyphsEditor::GetIsSideways","TRUE","xps.ixpsomglyphseditor_getissideways","xpsobjectmodel/IXpsOMGlyphsEditor::GetIsSideways"]
old-location: xps\ixpsomglyphseditor_getissideways.htm
tech.root: printdocs
ms.assetid: d115dbce-a81c-458f-8929-9e49e84a575d
ms.date: 12/05/2018
ms.keywords: FALSE, GetIsSideways, GetIsSideways method [XPS Documents and Packaging], GetIsSideways method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetIsSideways method, IXpsOMGlyphsEditor.GetIsSideways, IXpsOMGlyphsEditor::GetIsSideways, TRUE, xps.ixpsomglyphseditor_getissideways, xpsobjectmodel/IXpsOMGlyphsEditor::GetIsSideways
f1_keywords:
- xpsobjectmodel/IXpsOMGlyphsEditor.GetIsSideways
dev_langs:
- c++
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
- xpsobjectmodel.h
api_name:
- IXpsOMGlyphsEditor.GetIsSideways
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGlyphsEditor::GetIsSideways


## -description


Gets a Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.


## -parameters




### -param isSideways [out, retval]

The Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Rotate the glyphs sideways. Produces sideways text.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not rotate the glyphs sideways. Produces normal text.

</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>isSideways</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The default value for this property is <b>false</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

