---
UID: NF:gdiplusgraphics.Graphics.DrawCurve(IN const Pen,IN const Point,IN INT,IN REAL)
title: Graphics::DrawCurve(IN const Pen,IN const Point,IN INT,IN REAL) (gdiplusgraphics.h)
description: The Graphics::DrawCurve method draws a cardinal spline.
helpviewer_keywords: ["DrawCurve","DrawCurve method [GDI+]","DrawCurve method [GDI+]","Graphics class","Graphics class [GDI+]","DrawCurve method","Graphics.DrawCurve","Graphics.DrawCurve(IN const Pen","IN const Point","IN INT","IN REAL)","Graphics.DrawCurve(const Pen*","const Point*","INT","REAL)","Graphics::DrawCurve","Graphics::DrawCurve(IN const Pen","IN const Point","IN INT","IN REAL)","_gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_Point_points_INT_count_REAL_tension_","gdiplus._gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_Point_points_INT_count_REAL_tension_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_Point_points_INT_count_REAL_tension_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawcurvemethods\drawcurve_73penpen_pointpoints_intcount_realtensio.htm
ms.date: 12/05/2018
ms.keywords: DrawCurve, DrawCurve method [GDI+], DrawCurve method [GDI+],Graphics class, Graphics class [GDI+],DrawCurve method, Graphics.DrawCurve, Graphics.DrawCurve(IN const Pen,IN const Point,IN INT,IN REAL), Graphics.DrawCurve(const Pen*,const Point*,INT,REAL), Graphics::DrawCurve, Graphics::DrawCurve(IN const Pen,IN const Point,IN INT,IN REAL), _gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_Point_points_INT_count_REAL_tension_, gdiplus._gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_Point_points_INT_count_REAL_tension_
f1_keywords:
- gdiplusgraphics/Graphics.DrawCurve
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
- Graphics.DrawCurve
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::DrawCurve(IN const Pen,IN const Point,IN INT,IN REAL)


## -description


The <b>Graphics::DrawCurve</b> method draws a cardinal spline. 


## -parameters




### -param pen [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the cardinal spline. 


### -param points [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects that specify the coordinates that the cardinal spline passes through. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. 


### -param tension [in]

Type: <b>REAL</b>

Real number that specifies how tightly the curve bends through the coordinates of the cardinal spline. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Status</b> enumeration.




## -remarks



A segment is defined as a curve that connects two consecutive points in the cardinal spline. The ending point of each segment is the starting point for the next. 


#### Examples



The following example draws a cardinal spline.


```cpp
VOID Example_DrawCurve3(HDC hdc)
{
   Graphics graphics(hdc);

   // Define a Pen object and an array of Point objects.
   Pen greenPen(Color::Green, 3);
   Point point1(100, 100);
   Point point2(200, 50);
   Point point3(400, 10);
   Point point4(500, 100);
   
   Point curvePoints[4] = {
   point1,
   point2,
   point3,
   point4};

   Point* pcurvePoints = curvePoints;

   // Draw the curve.
   graphics.DrawCurve(&greenPen, curvePoints, 4, 1.0);

   //Draw the points in the curve.
   SolidBrush redBrush(Color::Red);
   graphics.FillEllipse(&redBrush, Rect(95, 95, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(195, 45, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(395, 5, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(495, 95, 10, 10));
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-cardinal-splines-about">Cardinal Splines</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpointf_inint_inreal)">DrawClosedCurve Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-drawing-cardinal-splines-use">Drawing Cardinal Splines</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
 

 

