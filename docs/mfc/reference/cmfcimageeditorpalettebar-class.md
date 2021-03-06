---
title: CMFCImageEditorPaletteBar-Klasse
ms.date: 11/04/2016
f1_keywords:
- CMFCImageEditorPaletteBar
- AFXIMAGEEDITORDIALOG/CMFCImageEditorPaletteBar
- AFXIMAGEEDITORDIALOG/CMFCImageEditorPaletteBar::GetRowHeight
- AFXIMAGEEDITORDIALOG/CMFCImageEditorPaletteBar::IsButtonExtraSizeAvailable
helpviewer_keywords:
- CMFCImageEditorPaletteBar [MFC], GetRowHeight
- CMFCImageEditorPaletteBar [MFC], IsButtonExtraSizeAvailable
ms.assetid: 3fb7ba8e-f254-4d56-b913-9941b4ed8138
ms.openlocfilehash: 71fe8824e7a7d250d9e939afea99f73fcb4943dd
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50498020"
---
# <a name="cmfcimageeditorpalettebar-class"></a>CMFCImageEditorPaletteBar-Klasse

Der Funktionsumfang Palette Balken zu einer Bild-Editor (Dialogfeld).

## <a name="syntax"></a>Syntax

```
class CMFCImageEditorPaletteBar : public CMFCToolBar
```

## <a name="members"></a>Member

### <a name="public-methods"></a>Öffentliche Methoden

|||
|-|-|
|Name|Beschreibung|
|[CMFCImageEditorPaletteBar::GetRowHeight](#getrowheight)|Gibt die Höhe von Symbolleisten-Schaltflächen. (Überschreibt [CMFCToolBar::GetRowHeight](../../mfc/reference/cmfctoolbar-class.md#getrowheight).)|
|[CMFCImageEditorPaletteBar::IsButtonExtraSizeAvailable](#isbuttonextrasizeavailable)|Bestimmt, ob die Symbolleiste Schaltflächen angezeigt werden kann, die Rahmen erweitert haben. (Überschreibt [CMFCToolBar::IsButtonExtraSizeAvailable](../../mfc/reference/cmfctoolbar-class.md#isbuttonextrasizeavailable).)|

### <a name="remarks"></a>Hinweise

Diese Klasse ist nicht vorgesehen, direkt aus Ihrem Code verwendet werden.

Das Framework verwendet diese Klasse, um eine Palette-Leiste in einem Bild-Editor-Dialogfeld angezeigt wird. Weitere Informationen zu diesem Bild-Editor-Dialogfeld finden Sie unter [CMFCImageEditorDialog-Klasse](../../mfc/reference/cmfcimageeditordialog-class.md).

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[CMFCBaseToolBa](../../mfc/reference/cmfcbasetoolbar-class.md)

[CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)

[CMFCImageEditorPaletteBar](../../mfc/reference/cmfcimageeditorpalettebar-class.md)

## <a name="requirements"></a>Anforderungen

**Header:** afximageeditordialog.h

##  <a name="getrowheight"></a>  CMFCImageEditorPaletteBar::GetRowHeight

Gibt die Höhe von Symbolleisten-Schaltflächen.

```
virtual int GetRowHeight() const;
```

### <a name="return-value"></a>Rückgabewert

Die Höhe der einzelnen Schaltflächen auf der Symbolleiste.

##  <a name="isbuttonextrasizeavailable"></a>  CMFCImageEditorPaletteBar::IsButtonExtraSizeAvailable

Bestimmt, ob die Symbolleiste Schaltflächen angezeigt werden kann, die Rahmen erweitert haben.

```
virtual BOOL IsButtonExtraSizeAvailable() const;
```

### <a name="return-value"></a>Rückgabewert

Diese Methode gibt FALSE zurück.

## <a name="see-also"></a>Siehe auch

[Hierarchiediagramm](../../mfc/hierarchy-chart.md)<br/>
[Klassen](../../mfc/reference/mfc-classes.md)<br/>
[CMFCImageEditorDialog-Klasse](../../mfc/reference/cmfcimageeditordialog-class.md)
