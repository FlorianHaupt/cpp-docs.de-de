---
title: Entwerfen von Auflistungs- und Enumeratorschnittstellen (ATL)
ms.date: 11/04/2016
helpviewer_keywords:
- enumerator interfaces
- collection interfaces
ms.assetid: ea19a39e-6333-41a1-be62-5435c236640e
ms.openlocfilehash: 8c7f782f52391b162a8b32a97961269178999ee0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50538202"
---
# <a name="design-principles-for-collection-and-enumerator-interfaces"></a>Entwurfsprinzipien für Auflistungs- und Enumeratorschnittstellen

Es gibt verschiedene Entwurfsprinzipien für jede Art von Schnittstelle:

- Stellt eine sammlungsschnittstelle *zufällige* Zugriff auf eine *einzelne* Element in der Auflistung über die `Item` -Methode, sie können Clients zu ermitteln, wie viele Elemente in der Auflistung über sind die `Count` Eigenschaft, und häufig ermöglicht Clients, Elemente hinzufügen und entfernen.

- Eine Enumeratorschnittstelle bereitstellt, *seriellen* Zugriff auf *mehrere* Elemente in einer Auflistung, es keine ermöglichen dem Client zu ermitteln, wie viele Elemente in der Auflistung sind (bis der Enumerator zurückgeben wird beendet. Elemente), und es bietet keine Möglichkeit zum Hinzufügen oder Entfernen von Elementen.

Jede Art von Schnittstelle spielt eine andere Rolle bei der Bereitstellung Zugriff auf die Elemente in einer Auflistung.

## <a name="see-also"></a>Siehe auch

[Auflistungen und-Enumerationen](../atl/atl-collections-and-enumerators.md)

