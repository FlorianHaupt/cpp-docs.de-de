---
title: CMFCRibbonCustomizeDialog-Klasse
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonCustomizeDialog
- AFXRIBBONCUSTOMIZEDIALOG/CMFCRibbonCustomizeDialog
- AFXRIBBONCUSTOMIZEDIALOG/CMFCRibbonCustomizeDialog::CMFCRibbonCustomizeDialog
helpviewer_keywords:
- CMFCRibbonCustomizeDialog [MFC], CMFCRibbonCustomizeDialog
ms.assetid: ce67de7f-5eaa-4c75-9b94-f290f36df073
ms.openlocfilehash: 2931bdc06f98f7031692a0e00fa9cbfb4136a657
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50542257"
---
# <a name="cmfcribboncustomizedialog-class"></a>CMFCRibbonCustomizeDialog-Klasse

Zeigt das Menüband **anpassen** Seite.

## <a name="syntax"></a>Syntax

```
class CMFCRibbonCustomizeDialog : public CMFCPropertySheet
```

## <a name="members"></a>Member

### <a name="public-constructors"></a>Öffentliche Konstruktoren

|Name|Beschreibung|
|----------|-----------------|
|[CMFCRibbonCustomizeDialog::CMFCRibbonCustomizeDialog](#cmfcribboncustomizedialog)|Erstellt ein `CMFCRibbonCustomizeDialog`-Objekt.|
|`CMFCRibbonCustomizeDialog::~CMFCRibbonCustomizeDialog`|Destruktor.|

### <a name="public-methods"></a>Öffentliche Methoden

|Name|Beschreibung|
|----------|-----------------|
|`CMFCRibbonCustomizeDialog::GetThisClass`|Durch das Framework verwendet wird, einen Zeiger zum Abrufen der [CRuntimeClass](../../mfc/reference/cruntimeclass-structure.md) -Objekt, das diesem Klassentyp zugeordnet ist.|

## <a name="remarks"></a>Hinweise

MFC instanziiert diese Klasse automatisch, wenn Sie keine die AFX_WM_ON_RIBBON_CUSTOMIZE Nachricht verarbeiten, oder wenn Sie 0 aus der Message-Handler zurückgegeben.

Wenn Sie diese Klasse in Ihrer Anwendung verwenden, um das Menüband anzeigen möchten **anpassen** Dialogfeld Feld, einfach zu instanziieren und Aufrufen der `DoModal` Methode.

Da von dieser Klasse abgeleitet ist [CMFCPropertySheet-Klasse](../../mfc/reference/cmfcpropertysheet-class.md), Sie können benutzerdefinierte Seiten hinzufügen, indem Sie mit der `CMFCPropertySheet` API.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CPropertySheet](../../mfc/reference/cpropertysheet-class.md)

[CMFCPropertySheet](../../mfc/reference/cmfcpropertysheet-class.md)

[CMFCRibbonCustomizeDialog](../../mfc/reference/cmfcribboncustomizedialog-class.md)

## <a name="requirements"></a>Anforderungen

**Header:** afxribboncustomizedialog.h

##  <a name="cmfcribboncustomizedialog"></a>  CMFCRibbonCustomizeDialog::CMFCRibbonCustomizeDialog

Erstellt ein `CMFCRibbonCustomizeDialog`-Objekt.

```
CMFCRibbonCustomizeDialog(
    CWnd* pWndParent,
    CMFCRibbonBar* pRibbon);
```

### <a name="parameters"></a>Parameter

*pWndParent*<br/>
[in] Ein Zeiger auf das übergeordnete Fenster (in der Regel den Hauptframe).

*pRibbon*<br/>
[in] Ein Zeiger auf die `CMFCRibbonBar` das heißt, die angepasst werden.

### <a name="example"></a>Beispiel

Das folgende Beispiel veranschaulicht das Erstellen einer `CMFCRibbonCustomizeDialog` Objekt.

[!code-cpp[NVC_MFC_RibbonApp#18](../../mfc/reference/codesnippet/cpp/cmfcribboncustomizedialog-class_1.cpp)]

### <a name="remarks"></a>Hinweise

Der Konstruktor instanziiert ein [CMFCRibbonCustomizePropertyPage-Klasse](../../mfc/reference/cmfcribboncustomizepropertypage-class.md) Objekt und die Auflistung der Eigenschaftenblattseiten hinzugefügt.

## <a name="see-also"></a>Siehe auch

[Hierarchiediagramm](../../mfc/hierarchy-chart.md)<br/>
[Klassen](../../mfc/reference/mfc-classes.md)
