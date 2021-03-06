---
title: CMFCToolBarInfo-Klasse
ms.date: 11/04/2016
f1_keywords:
- CMFCToolBarInfo
- AFXTOOLBAR/CMFCToolBarInfo
- AFXTOOLBAR/CMFCToolBarInfo::m_uiColdResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiDisabledResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiHotResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiLargeColdResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiLargeDisabledResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiLargeHotResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiMenuDisabledResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiMenuResID
helpviewer_keywords:
- CMFCToolBarInfo [MFC], m_uiColdResID
- CMFCToolBarInfo [MFC], m_uiDisabledResID
- CMFCToolBarInfo [MFC], m_uiHotResID
- CMFCToolBarInfo [MFC], m_uiLargeColdResID
- CMFCToolBarInfo [MFC], m_uiLargeDisabledResID
- CMFCToolBarInfo [MFC], m_uiLargeHotResID
- CMFCToolBarInfo [MFC], m_uiMenuDisabledResID
- CMFCToolBarInfo [MFC], m_uiMenuResID
ms.assetid: 6dc84482-eaaa-491f-aa5d-dd7a57886b46
ms.openlocfilehash: e1e460fe3efb5401227e91f49d8f7c4f6689fa27
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50651164"
---
# <a name="cmfctoolbarinfo-class"></a>CMFCToolBarInfo-Klasse

Enthält die Ressourcen-IDs von Symbolleistenbildern in unterschiedlichen Zuständen. `CMFCToolBarInfo` ist eine Hilfsklasse, die als Parameter verwendet, wird die [cmfctoolbar:: Loadtoolbarex](../../mfc/reference/cmfctoolbar-class.md#loadtoolbarex) Methode.

## <a name="syntax"></a>Syntax

```
class CMFCToolBarInfo
```

## <a name="members"></a>Member

### <a name="data-members"></a>Datenmember

|name|Beschreibung|
|----------|-----------------|
|[CMFCToolBarInfo::m_uiColdResID](#m_uicoldresid)|Ressourcen-ID der Symbolleistenbitmap für die, die reguläre (kalte) Symbolleistenbilder enthält.|
|[CMFCToolBarInfo::m_uiDisabledResID](#m_uidisabledresid)|Ressourcen-ID der Symbolleistenbitmap für die, die deaktivierten Symbolleistenbilder enthält.|
|[CMFCToolBarInfo::m_uiHotResID](#m_uihotresid)|Ressourcen-ID der Symbolleistenbitmap für die, die ausgewählte (hot) Symbolleistenbilder enthält.|
|[CMFCToolBarInfo::m_uiLargeColdResID](#m_uilargecoldresid)|Ressourcen-ID der Symbolleistenbitmap für die, die große, reguläre Symbolleistenbilder enthält.|
|[CMFCToolBarInfo::m_uiLargeDisabledResID](#m_uilargedisabledresid)|Ressourcen-ID der Symbolleistenbitmap für die, die große enthält deaktiviert Symbolleistenbilder.|
|[CMFCToolBarInfo::m_uiLargeHotResID](#m_uilargehotresid)|Ressourcen-ID der Symbolleistenbitmap für die, die große, ausgewählten Symbolleistenbilder enthält.|
|[CMFCToolBarInfo::m_uiMenuDisabledResID](#m_uimenudisabledresid)|Ressourcen-ID der Symbolleistenbitmap für die, die deaktivierten Menübilder enthält.|
|[CMFCToolBarInfo::m_uiMenuResID](#m_uimenuresid)|Ressourcen-ID der Symbolleistenbitmap für die, die im Menübilder enthält.|

## <a name="remarks"></a>Hinweise

Eine Bitmap für die vollständige Symbolleiste bestehen aus kleinen Symbolleistenbilder (Schaltflächen) eine feste Größe. Jede Ressource-ID, die in gespeichert ist eine `CMFCToolBarInfo` Objekt ist eine Bitmap, die einen vollständigen Satz von symbolleistenbildern in einem Zustand (z. B., ausgewählt "," deaktiviert "," Groß "oder" Menübilder ") enthält.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[CMFCToolBarInfo](../../mfc/reference/cmfctoolbarinfo-class.md)

## <a name="requirements"></a>Anforderungen

**Header:** afxtoolbar.h

##  <a name="m_uicoldresid"></a>  CMFCToolBarInfo::m_uiColdResID

Gibt eine Ressourcen-ID für alle Bilder, die normale Schaltfläche einer Symbolleiste an.

```
UINT m_uiColdResID;
```

##  <a name="m_uidisabledresid"></a>  CMFCToolBarInfo::m_uiDisabledResID

Gibt eine Ressourcen-ID für die Schaltfläche nicht verfügbar ist-Images von einer Symbolleiste an.

```
UINT m_uiDisabledResID;
```

##  <a name="m_uihotresid"></a>  CMFCToolBarInfo::m_uiHotResID

Gibt eine Ressourcen-ID für alle Bilder der hervorgehobenen Schaltfläche einer Symbolleiste an.

```
UINT m_uiHotResID
```

##  <a name="m_uilargecoldresid"></a>  CMFCToolBarInfo::m_uiLargeColdResID

Gibt eine Ressourcen-ID für alle Bilder, die große normale Schaltfläche einer Symbolleiste an.

```
UINT m_uiLargeColdResID
```

##  <a name="m_uilargedisabledresid"></a>  CMFCToolBarInfo::m_uiLargeDisabledResID

Gibt eine Ressourcen-ID für alle Bilder, die große deaktivierte Schaltfläche einer Symbolleiste an.

```
UINT m_uiLargeDisabledResID;
```

##  <a name="m_uilargehotresid"></a>  CMFCToolBarInfo::m_uiLargeHotResID

Gibt eine Ressourcen-ID für alle großen hervorgehobenen Bilder von einer Symbolleiste an.

```
UINT m_uiLargeHotResID;
```

##  <a name="m_uimenudisabledresid"></a>  CMFCToolBarInfo::m_uiMenuDisabledResID

Gibt eine Ressourcen-ID für die Bilder Befehl nicht verfügbar ist, einer Symbolleiste an.

```
UINT m_uiMenuDisabledResID;
```

##  <a name="m_uimenuresid"></a>  CMFCToolBarInfo::m_uiMenuResID

Gibt eine Ressourcen-ID für alle regulären menüelementbilder einer Symbolleiste an.

```
UINT m_uiMenuResID;
```

## <a name="see-also"></a>Siehe auch

[Hierarchiediagramm](../../mfc/hierarchy-chart.md)<br/>
[Klassen](../../mfc/reference/mfc-classes.md)<br/>
[CMFCToolBar-Klasse](../../mfc/reference/cmfctoolbar-class.md)
