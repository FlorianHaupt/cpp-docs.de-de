---
title: 'NMAKE: Warnung U4011'
ms.date: 11/04/2016
f1_keywords:
- U4011
helpviewer_keywords:
- U4011
ms.assetid: e8244514-eba6-4285-8853-7baeefdcd8a4
ms.openlocfilehash: 3b73e92c929b3dd5924584ab732f731d565d0430
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50428443"
---
# <a name="nmake-warning-u4011"></a>NMAKE: Warnung U4011

'Target': nicht alle abhängigen Elemente verfügbar. Ziel nicht erstellt

Das angegebene Ziel ein abhängiges Element ist nicht vorhanden oder war nicht mehr aktuell, und ein Befehl zum Aktualisieren des abhängigen zurückgegeben einen Exitcode ungleich NULL. Die Option/k mitgeteilt NMAKE und weiter verarbeitet, nicht zusammengehöriger Teile des Builds und einen Exitcode 1 auszugeben, die NMAKE-Sitzung abgeschlossen ist.

Diese Warnung wird für die Warnung vorangestellt [U4010](../../error-messages/tool-errors/nmake-warning-u4010.md) für jedes abhängige, die nicht erstellt oder aktualisiert werden konnten.