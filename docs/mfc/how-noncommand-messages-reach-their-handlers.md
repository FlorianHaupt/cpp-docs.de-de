---
title: Wie nicht befehlsbasierte Meldungen ihre Handler erreichen
ms.date: 11/04/2016
helpviewer_keywords:
- messages [MFC], routing
- noncommand messages
- Windows messages [MFC], routing
- message handling [MFC], noncommand messages
ms.assetid: e7df8aef-9fae-41f4-9c11-881d8465f602
ms.openlocfilehash: f64eb97315b41a314c791e1a4c5bc7721b329fca
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50545456"
---
# <a name="how-noncommand-messages-reach-their-handlers"></a>Wie nicht befehlsbasierte Meldungen ihre Handler erreichen

Im Gegensatz zu den Befehlen standard-Windows-Nachrichten werden nicht durch eine Kette von Befehlsziele weitergeleitet, aber erfolgt in der Regel durch das Fenster, die an den Windows die Nachricht sendet. Das Fenster möglicherweise ein Hauptrahmenfenster, eines untergeordneten MDI-Fensters, ein Standardsteuerelement, ein Dialogfeld, eine Sicht oder eine andere Art von untergeordneten Fensters.

Bei der Ausführung jedes Windows-Fenster an ein Window-Objekt angefügt ist (direkt oder indirekt von abgeleiteten `CWnd`), die eigene Funktionen zugeordnete Meldung, Zuordnung und der Handler hat. Das Framework verwendet die meldungszuordnung – wie für einen Befehl, eingehende Nachrichten an die Handler zugeordnet.

## <a name="see-also"></a>Siehe auch

[So ruft das Framework einen Handler auf](../mfc/how-the-framework-calls-a-handler.md)

