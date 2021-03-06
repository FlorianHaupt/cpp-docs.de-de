---
title: Registrierungseinträge (ATL)
ms.date: 11/04/2016
helpviewer_keywords:
- registry, ATL services entries
- registry, application IDs
ms.assetid: 881989b7-61bb-459a-a13e-3bfcb33e184e
ms.openlocfilehash: b61aae9ba9316dded1dcb11353e52eb2fffd49a2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50472877"
---
# <a name="registry-entries"></a>Registrierungseinträge

DCOM wurde das Konzept von Anwendungs-IDs (AppIDs), welcher Gruppe Konfigurationsoptionen für eine oder mehrere DCOM-Objekte in einem zentralen Ort in der Registrierung eingeführt. Sie geben eine AppID, der angibt, dessen Wert in die App-ID mit dem Namen Wert unter der CLSID des Objekts.

Standardmäßig verwendet einen ATL generierte-Dienst als GUID seines CLSID für die App-ID an. Klicken Sie unter `HKEY_CLASSES_ROOT\AppID`, können Sie die DCOM-spezifische Einträge angeben. Anfänglich sind zwei Einträge vorhanden:

- `LocalService`, mit dem Wert, der gleich dem Namen des Diensts. Wenn dieser Wert vorhanden ist, wird es verwendet, statt die `LocalServer32` Schlüssel unter der CLSID.

- `ServiceParameters`, mit dem Wert, der gleich `-Service`. Dieser Wert gibt die Parameter, die an den Dienst übergeben werden, wenn es gestartet wird. Beachten Sie, die diese Parameter an des Diensts übergeben werden `ServiceMain` funktionieren, nicht `WinMain`.

Außerdem muss jeder DCOM-Dienst erstellen Sie einen weiteren Schlüssel unter `HKEY_CLASSES_ROOT\AppID`. Dieser Schlüssel ist gleich dem Namen der EXE-Datei und fungiert als Querverweis, da er einen AppID-Wert, der zurück auf die App-ID-Einträge enthält.

## <a name="see-also"></a>Siehe auch

[Dienste](../atl/atl-services.md)

