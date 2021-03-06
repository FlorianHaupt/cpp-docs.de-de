---
title: Steuerelementtypen für die Symbolleiste
ms.date: 11/04/2016
helpviewer_keywords:
- ToolBar control styles [MFC]
ms.assetid: 0f717eb9-fa32-4263-b852-809238863feb
ms.openlocfilehash: f26edc6c0ce4a19528a9a8754428411318e9b9d2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50648993"
---
# <a name="toolbar-control-styles"></a>Steuerelementtypen für die Symbolleiste

[CMFCToolBarButton-Klasse](../../mfc/reference/cmfctoolbarbutton-class.md) verfügt über einen Satz von Style Flags, die bestimmen, die Darstellung und Verhalten der Schaltfläche. Sie können eine Kombination dieser Flags festlegen, durch den Aufruf [CMFCToolBarButton::SetStyle](../../mfc/reference/cmfctoolbarbutton-class.md#setstyle). Dieses Thema enthält die Style-Flagwerte und ihre Bedeutung.

## <a name="property-values"></a>Eigenschaftswerte

Die folgenden Werte bestimmen den Typ der Schaltfläche, die das Steuerelement darstellt:

|||
|-|-|
|TBBS_BUTTON|Standardmäßige Pushbutton (Standard).  |
|TBBS_CHECKBOX|Das Kontrollkästchen.  |
|TBBS_CHECKGROUP|Der Anfang einer Gruppe von Kontrollkästchen.  |
|TBBS_GROUP|Der Anfang einer Gruppe von Schaltflächen.  |
|TBBS_SEPARATOR|Trennzeichen.  |

Die folgenden Werte stellen den aktuellen Status des Steuerelements dar:

|||
|-|-|
|TBBS_CHECKED|Aktivieren Sie das Kontrollkästchen aktiviert ist.  |
|TBBS_DISABLED|Das Steuerelement ist deaktiviert.  |
|TBBS_INDETERMINATE|Aktivieren Sie das Kontrollkästchen ist in einem unbestimmten Zustand.  |
|TBBS_PRESSED|Schaltfläche ist gedrückt.  |

Der folgende Wert ändert das Layout der Schaltfläche auf der Symbolleiste:

|||
|-|-|
|TBBS_BREAK|Platziert das Element in einer neuen Zeile oder in einer neuen Spalte ohne Trennen von Spalten.  |

## <a name="remarks"></a>Hinweise

Der aktuelle Stil befindet sich in [CMFCToolBarButton::m_nStyle](../../mfc/reference/cmfctoolbarbutton-class.md#m_nstyle). Legen Sie einen neuen Wert nicht in `m_nStyle` direkt, da die abgeleiteten Klassen Durchführung weiterer Bearbeitungsvorgänge, wenn Sie aufrufen `SetStyles`.

Visuelle Manager bestimmt die Darstellung der Schaltflächen in den einzelnen Zuständen. Finden Sie unter [Visualisierungs-Manager](../../mfc/visualization-manager.md) für Weitere Informationen.

## <a name="requirements"></a>Anforderungen

**Header:** afxtoolbarbutton.h

## <a name="see-also"></a>Siehe auch

[Makros und globale Variablen](../../mfc/reference/mfc-macros-and-globals.md)<br/>
[CMFCToolBarButton-Klasse](../../mfc/reference/cmfctoolbarbutton-class.md)<br/>
[Visualisierungs-Manager](../../mfc/visualization-manager.md)

