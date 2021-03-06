---
title: CHtmlEditView-Klasse
ms.date: 11/04/2016
f1_keywords:
- CHtmlEditView
- AFXHTML/CHtmlEditView
- AFXHTML/CHtmlEditView::CHtmlEditView
- AFXHTML/CHtmlEditView::Create
- AFXHTML/CHtmlEditView::GetDHtmlDocument
- AFXHTML/CHtmlEditView::GetStartDocument
helpviewer_keywords:
- CHtmlEditView [MFC], CHtmlEditView
- CHtmlEditView [MFC], Create
- CHtmlEditView [MFC], GetDHtmlDocument
- CHtmlEditView [MFC], GetStartDocument
ms.assetid: 166c8ba8-3fb5-4dd7-a9ea-5bca662d00f6
ms.openlocfilehash: 9df4aa2b2418995f6e012c0baefb6dc8918eaee8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50559782"
---
# <a name="chtmleditview-class"></a>CHtmlEditView-Klasse

Stellt die Funktionalität der WebBrowser-Bearbeitungsplattform im Kontext der MFC-Dokument-/Ansichtarchitektur bereit.

## <a name="syntax"></a>Syntax

```
class CHtmlEditView : public CHtmlView, public CHtmlEditCtrlBase<CHtmlEditView>
```

## <a name="members"></a>Member

### <a name="public-constructors"></a>Öffentliche Konstruktoren

|Name|Beschreibung|
|----------|-----------------|
|[CHtmlEditView::CHtmlEditView](#chtmleditview)|Erstellt ein `CHtmlEditView`-Objekt.|

### <a name="public-methods"></a>Öffentliche Methoden

|Name|Beschreibung|
|----------|-----------------|
|[CHtmlEditView::Create](#create)|Erstellt ein neues Fensterobjekt.|
|[CHtmlEditView::GetDHtmlDocument](#getdhtmldocument)|Gibt die `IHTMLDocument2` Schnittstelle für das aktuelle Dokument.|
|[CHtmlEditView::GetStartDocument](#getstartdocument)|Ruft den Namen das Standarddokument für diese Ansicht ab.|

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CView](../../mfc/reference/cview-class.md)

[CScrollView](../../mfc/reference/cscrollview-class.md)

[CFormView](../../mfc/reference/cformview-class.md)

[CHtmlEditCtrlBase](../../mfc/reference/chtmleditctrlbase-class.md)

[CHtmlView](../../mfc/reference/chtmlview-class.md)

`CHtmlEditView`

## <a name="requirements"></a>Anforderungen

**Header:** afxhtml.h

##  <a name="chtmleditview"></a>  CHtmlEditView::CHtmlEditView

Erstellt ein `CHtmlEditView`-Objekt.

```
CHtmlEditView();
```

##  <a name="create"></a>  CHtmlEditView::Create

Erstellt ein neues Fensterobjekt.

```
virtual BOOL Create(
    LPCTSTR lpszClassName,
    LPCTSTR lpszWindowName,
    DWORD dwStyle,
    const RECT& rect,
    CWnd* pParentWnd,
    UINT nID,
    CCreateContext* pContext = NULL);
```

### <a name="parameters"></a>Parameter

*"lpszclassname"*<br/>
Verweist auf eine Null-terminierte Zeichenfolge, die Namen die Windows-Klasse. Der Klassenname kann einen beliebigen Namen registriert werden die [AfxRegisterWndClass](application-information-and-management.md#afxregisterwndclass) globale Funktion oder die `RegisterClass` Windows-Funktion. Wenn der Wert NULL ist, verwendet den vordefinierten Standardwert [CFrameWnd](../../mfc/reference/cframewnd-class.md) Attribute.

*lpszWindowName*<br/>
Verweist auf eine Null-terminierte Zeichenfolge, die den Fensternamen darstellt.

*dwStyle*<br/>
Gibt an, der die Stilattribute für Fenster. Standardmäßig werden die Stile WS_VISIBLE und WS_CHILD Windows festgelegt.

*Rect*<br/>
Ein Verweis auf eine [RECT](https://msdn.microsoft.com/library/windows/desktop/dd162897) -Struktur, die die Größe und Position des Fensters angibt. Die *RectDefault* Wert ermöglicht Windows die Größe und Position des neuen Fensters an.

*pParentWnd*<br/>
Ein Zeiger auf das übergeordnete Fenster des Steuerelements.

*nID*<br/>
Die ID der Sicht. Legen Sie in der Standardeinstellung auf AFX_IDW_PANE_FIRST.

*pContext*<br/>
Ein Zeiger auf eine [CCreateContext](../../mfc/reference/ccreatecontext-structure.md). Standardmäßig NULL.

### <a name="remarks"></a>Hinweise

Diese Methode wird auch die eigenständigen WebBrowser Aufrufen `Navigate` Methode, um ein Standarddokument laden (finden Sie unter [CHtmlEditView::GetStartDocument](#getstartdocument)).

##  <a name="getdhtmldocument"></a>  CHtmlEditView::GetDHtmlDocument

Gibt die `IHTMLDocument2` Schnittstelle für das aktuelle Dokument.

```
BOOL GetDHtmlDocument(IHTMLDocument2** ppDocument) const;
```

### <a name="parameters"></a>Parameter

*ppDocument*<br/>
Die [IHTMLDocument2](https://msdn.microsoft.com/library/aa752574.aspx) Schnittstelle.

##  <a name="getstartdocument"></a>  CHtmlEditView::GetStartDocument

Ruft den Namen das Standarddokument für diese Ansicht ab.

```
virtual LPCTSTR GetStartDocument();
```

## <a name="see-also"></a>Siehe auch

[HTMLEdit-Beispiel](../../visual-cpp-samples.md)<br/>
[Hierarchiediagramm](../../mfc/hierarchy-chart.md)

