---
title: struct RUNTIME_FUNCTION
ms.date: 11/04/2016
ms.assetid: 84386527-d3aa-41c5-871d-78e3e1913704
ms.openlocfilehash: 6b113f6cf1e9951f9e4578e15c9ed0af3d036fa6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50520249"
---
# <a name="struct-runtimefunction"></a>struct RUNTIME_FUNCTION

Tabellenbasierte Ausnahmebehandlung erfordert Tabelleneintrag für alle Funktionen, die Stapelspeicherplatz belegt werden, oder rufen Sie eine andere Funktion (z. B. Nichtblattelemente Funktionen). Funktion-Tabelleneinträge aufweisen Folgendes Format:

|||
|-|-|
|ULONG|Startadresse der Funktion|
|ULONG|Funktion-Endadresse|
|ULONG|Adresse der Entladeinformationen|

Die Struktur RUNTIME_FUNCTION muss DWORD im Arbeitsspeicher ausgerichtet sein. Alle Adressen sind relative-Image, d. h. 32-Bit-abweichungen von der die Startadresse des Bilds, das den Funktionstabelleneintrag enthält. Diese Einträge sind sortiert, und fügen Sie in den .pdata-Abschnitt eines Images PE32 +. Für dynamisch generierte Funktionen [JIT-Compiler] muss die Laufzeit zur Unterstützung dieser Funktionen entweder RtlInstallFunctionTableCallback oder RtlAddFunctionTable verwenden diese Informationen für das Betriebssystem bereitstellen. Bei unterlassen führt zu unzuverlässigen Behandlung von Ausnahmen und Debuggen von Prozessen.

## <a name="see-also"></a>Siehe auch

[Entladedaten für die Ausnahmebehandlung, Debuggerunterstützung](../build/unwind-data-for-exception-handling-debugger-support.md)