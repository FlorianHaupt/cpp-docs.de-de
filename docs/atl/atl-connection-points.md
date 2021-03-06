---
title: ATL-Verbindungspunkte
ms.date: 11/04/2016
helpviewer_keywords:
- connections, connection points
- ATL, connection points
- connection points [C++], about connection points
ms.assetid: 17d76165-5f83-4f95-b36d-483821c247a1
ms.openlocfilehash: 520537f5d562450dc4ea2a5e5a0c68af513da509
ms.sourcegitcommit: 9e891eb17b73d98f9086d9d4bfe9ca50415d9a37
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2018
ms.locfileid: "52175055"
---
# <a name="atl-connection-points"></a>ATL-Verbindungspunkte

Ein verbindungsfähiges Objekt ist eines, das Ausgangsschnittstellen unterstützt. Eine Ausgangsschnittstelle ermöglicht dem Objekt die Kommunikation mit einem Client. Für jede Ausgangsschnittstelle macht das verbindungsfähige Objekt einen Verbindungspunkt verfügbar. Jede Ausgangsschnittstelle wird von einem Client auf einem Objekt, das als Sink bezeichnet wird, implementiert.

![Verbindungspunkte](../atl/media/vc2zw31.gif "Verbindungspunkte")

Jeder Verbindungspunkt unterstützt die [IConnectionPoint](/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint) Schnittstelle. Das verbindungsfähige Objekt macht seine Verbindungspunkte auf dem Client über die [IConnectionPointContainer](/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer) Schnittstelle.

## <a name="in-this-section"></a>In diesem Abschnitt

[ATL-Connection Point-Klassen](../atl/atl-connection-point-classes.md)<br/>
Beschreibt kurz die ATL-Klassen, die Verbindungspunkte unterstützen.

[Hinzufügen von Verbindungspunkten zu einem Objekt](../atl/adding-connection-points-to-an-object.md)<br/>
Beschreibt die Schritte, um einem Objekt Verbindungspunkte hinzuzufügen.

[Beispiel für ATL-Verbindungspunkt](../atl/atl-connection-point-example.md)<br/>
Enthält ein Beispiel für das Deklarieren eines Verbindungspunktes.

## <a name="related-sections"></a>Verwandte Abschnitte

[ATL](../atl/active-template-library-atl-concepts.md)<br/>
Enthält Links zu konzeptionellen Themen über die Programmierung mit der Active Template Library.

## <a name="see-also"></a>Siehe auch

[Konzepte](../atl/active-template-library-atl-concepts.md)

