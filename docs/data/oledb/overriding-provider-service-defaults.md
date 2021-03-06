---
title: Überschreiben der Standardwerte für Anbieterdienste
ms.date: 10/29/2018
helpviewer_keywords:
- service providers [OLE DB]
- OLE DB services [OLE DB], overriding defaults
ms.assetid: 08e366c0-74d8-463b-93a6-d58a8dc195f8
ms.openlocfilehash: 9f845834b844c16bf2820a295768696e8f6a6526
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556295"
---
# <a name="overriding-provider-service-defaults"></a>Überschreiben der Standardwerte für Anbieterdienste

Der Anbieter Registrierungswert für OLEDB_SERVICES wird zurückgegeben, als der Standardwert für die [DBPROP_INIT_OLEDBSERVICES](https://docs.microsoft.com/previous-versions/windows/desktop/ms716898(v=vs.85)) -Eigenschaft zur datenquelleninitialisierung auf das Datenquellenobjekt.

Solange der Registrierungseintrag vorhanden ist, wird die Anbieterobjekte aggregiert. Der Benutzer kann der Anbieter Standardeinstellung für die aktivierten Dienste durch Festlegen der Eigenschaft DBPROP_INIT_OLEDBSERVICES vor der Initialisierung überschreiben. Zum Aktivieren oder deaktivieren einen bestimmten Dienst, der Benutzer ruft den aktuellen Wert der Eigenschaft DBPROP_INIT_OLEDBSERVICES festlegt oder löscht das Bit für die betreffende Eigenschaft aktiviert bzw. deaktiviert werden soll, und setzt die Eigenschaft zurück. DBPROP_INIT_OLEDBSERVICES kann festgelegt werden, direkt in der OLE DB oder in der Verbindungszeichenfolge, die an ADO oder `IDataInitialize::GetDatasource`. Die entsprechenden Werte zum Aktivieren/Deaktivieren einzelner Dienste werden in der folgenden Tabelle aufgeführt.

|Standarddienste, die aktiviert|DBPROP_INIT_OLEDBSERVICES-Eigenschaftswert|Wert in der Verbindungszeichenfolge|
|------------------------------|------------------------------------------------|--------------------------------|
|Alle Dienste (Standard)|DBPROPVAL_OS_ENABLEALL|"OLE DB-Diensten =-1;"|
|Alle außer Pooling und AutoEnlistment|`DBPROPVAL_OS_ENABLEALL &`<br /><br /> `~DBPROPVAL_OS_RESOURCEPOOLING &`<br /><br /> `~DBPROPVAL_OS_TXNENLISTMENT`|"OLE DB-Diensten-4; ="|
|Alle außer den Clientcursor|`DBPROPVAL_OS_ENABLEALL &`<br /><br /> `~DBPROPVAL_OS_CLIENTCURSOR`|"OLE DB-Diensten-5; ="|
|Alle außer Pooling AutoEnlistment und Clientcursor|`DBPROPVAL_OS_ENABLEALL &`<br /><br /> `~DBPROPVAL_OS_TXNENLISTMENT &`<br /><br /> `~DBPROPVAL_OS_CLIENTCURSOR`|"OLE DB-Diensten-7; ="|
|Keine Dienste|`~DBPROPVAL_OS_ENABLEALL`|"OLE DB-Diensten = 0;"|

Wenn der Registrierungseintrag für den Anbieter nicht vorhanden ist, wird nicht die Komponenten-Manager des Anbieters Objekten sammeln. Keine Dienste werden aktiviert, selbst wenn explizit vom Benutzer angefordert.

## <a name="see-also"></a>Siehe auch

[Ressourcenpooling](https://docs.microsoft.com/previous-versions/windows/desktop/ms713655(v=vs.85))<br/>
[Verwendung Kunden, die Ressourcenpooling](https://docs.microsoft.com/previous-versions/windows/desktop/ms715907(v=vs.85))<br/>
[Funktionsweise von Anbietern effektiv mit Ressourcenpooling](https://docs.microsoft.com/previous-versions/windows/desktop/ms714906(v=vs.85))<br/>
[Aktivieren und Deaktivieren von OLE DB-Diensten](../../data/oledb/enabling-and-disabling-ole-db-services.md)<br/>