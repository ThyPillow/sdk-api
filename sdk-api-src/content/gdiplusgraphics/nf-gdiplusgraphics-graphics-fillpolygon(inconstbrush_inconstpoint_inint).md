---
UID: NF:gdiplusgraphics.Graphics.FillPolygon(IN const Brush,IN const Point,IN INT)
title: Graphics::FillPolygon(IN const Brush,IN const Point,IN INT) (gdiplusgraphics.h)
description: The Graphics::FillPolygon method uses a brush to fill the interior of a polygon.
helpviewer_keywords: ["FillPolygon","FillPolygon method [GDI+]","FillPolygon method [GDI+]","Graphics class","Graphics class [GDI+]","FillPolygon method","Graphics.FillPolygon","Graphics.FillPolygon(IN const Brush","IN const Point","IN INT)","Graphics.FillPolygon(const Brush*","const Point*","INT)","Graphics::FillPolygon","Graphics::FillPolygon(IN const Brush","IN const Point","IN INT)","_gdiplus_CLASS_Graphics_FillPolygon_Brush_brush_Point_points_INT_count_","gdiplus._gdiplus_CLASS_Graphics_FillPolygon_Brush_brush_Point_points_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillPolygon_Brush_brush_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillpolygonmethods\fillpolygon.htm
ms.date: 12/05/2018
ms.keywords: FillPolygon, FillPolygon method [GDI+], FillPolygon method [GDI+],Graphics class, Graphics class [GDI+],FillPolygon method, Graphics.FillPolygon, Graphics.FillPolygon(IN const Brush,IN const Point,IN INT), Graphics.FillPolygon(const Brush*,const Point*,INT), Graphics::FillPolygon, Graphics::FillPolygon(IN const Brush,IN const Point,IN INT), _gdiplus_CLASS_Graphics_FillPolygon_Brush_brush_Point_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_FillPolygon_Brush_brush_Point_points_INT_count_
f1_keywords:
- gdiplusgraphics/Graphics.FillPolygon
dev_langs:
- c++
req.header: gdiplusgraphics.h
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
- Graphics.FillPolygon
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::FillPolygon(IN const Brush,IN const Point,IN INT)


## -description


The <b>Graphics::FillPolygon</b> method uses a brush to fill the interior of a polygon. 


## -parameters




### -param brush [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to paint the interior of the polygon. 


### -param points [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of points that make up the vertices of the polygon. The first two points in the array specify the first side of the polygon. Each additional point specifies a new side, the vertices of which include the point and the previous point. If the last point and the first point do not coincide, they specify the last side of the polygon. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of points in the <i>points</i> array. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
 

 

