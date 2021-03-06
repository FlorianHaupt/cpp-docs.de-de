---
title: OLE DB-Consumer und -Anbieter
ms.date: 10/22/2018
helpviewer_keywords:
- OLE DB providers, OLE DB data architecture
- OLE DB providers
- OLE DB consumers, OLE DB data architecture
- OLE DB consumers
- OLE DB, data model
ms.assetid: 886cb39d-652b-4557-93f0-4b1b0754d8bc
ms.openlocfilehash: 65e4cf9dcade897a346e8f9bbc1985f9edede78e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50443393"
---
# <a name="ole-db-consumers-and-providers"></a>OLE DB-Consumer und -Anbieter

Die OLE DB-Architektur verwendet das Modell von Consumern und Anbietern. Ein Consumer sendet Anforderungen für Daten. Ein Anbieter reagiert auf diese Anforderungen durch die Platzierung von Daten in einem tabellarischen Format und diese an den Consumer zurückgegeben wird. Alle Aufrufe, die der Consumer vornehmen können, muss im Anbieter implementiert werden.

Aus technischer Sicht definiert ist, ist ein Consumer System- oder Code (nicht unbedingt eine OLE DB-Komponente), die über OLE DB-Schnittstellen auf Daten zugreift. Die Schnittstellen sind in einem Anbieter implementiert. Daher ist ein Anbieter eine beliebige Softwarekomponente, die implementiert die OLE DB-Schnittstellen zum Zugriff auf Daten zu kapseln und anderen Objekten (d. h. Verbraucher) verfügbar gemacht.

Für Rollen Ruft ein Consumer Methoden auf OLE DB-Schnittstellen; OLE DB-Anbieter implementiert die erforderlichen OLE DB-Schnittstellen.

OLE DB werden Begriffe-Client und Server vermieden, da diese Rollen immer, insbesondere in einer n-schichtige Situation nicht sinnvoll sind. Da ein Consumer eine Komponente in einer Ebene, die eine andere Komponente dient sein kann, wird für den Aufruf eines Clients Komponente verwirrend sein. Darüber hinaus verhält sich ein Anbieter manchmal eher wie ein ODBC-Treiber als bei einem Server.

## <a name="see-also"></a>Siehe auch

[OLE DB-Programmierung](../../data/oledb/ole-db-programming.md)<br/>
[Übersicht über die OLE DB-Programmierung](../../data/oledb/ole-db-programming-overview.md)