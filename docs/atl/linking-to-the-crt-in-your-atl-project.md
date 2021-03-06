---
title: Verknüpfen mit der CRT in einem ATL-Projekt
ms.date: 11/04/2016
f1_keywords:
- DllMainCRTStartup
- wWinMainCRTStartup
- WinMainCRTStartup
helpviewer_keywords:
- CRT, linking with ATL
- WinMainCRTStartup method
- DllMainCRTStartup method
- wWinMainCRTStartup method
- ATL, C Run-Time library (CRT)
ms.assetid: 650957ae-362c-4ecf-8b03-5d49138e8b5b
ms.openlocfilehash: fc8c3c591b04d62c6dd7cf72bedde7a668e9f146
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50516452"
---
# <a name="linking-to-the-crt-in-your-atl-project"></a>Verknüpfen mit der CRT in einem ATL-Projekt

Die [C-Laufzeitbibliotheken](../c-runtime-library/crt-library-features.md) (CRT) bieten zahlreiche nützliche Funktionen, die während der Entwicklung von ATL-Programmierung wesentlich einfacher vornehmen können. Alle ATL-Projekte, die mit der CRT-Bibliothek verknüpft werden. Sehen Sie die vor- und Nachteile der Methode in der Verknüpfung [vor- und Nachteile der Methode verwendet, um die Verknüpfung mit der CRT](../atl/benefits-and-tradeoffs-of-the-method-used-to-link-to-the-crt.md).

## <a name="effects-of-linking-to-the-crt-on-your-program-image"></a>Auswirkungen der Verknüpfung mit der CRT in Ihr Programmimage

Wenn Sie mit der CRT statisch verknüpft, Code aus der CRT befindet sich in Ihre ausführbaren Images, und Sie müssen sich nicht um die CRT-DLL vorhanden auf einem System, führen Sie das Abbild zu erhalten. Wenn Sie dynamisch mit der CRT verknüpfen, werden Verweise auf den Code in der CRT-DLL in das Image, aber nicht den Code selbst platziert. In der Reihenfolge für Ihr Image auf einem bestimmten System ausgeführt wird muss die CRT-DLL auf dem System vorhanden sein. Auch wenn Sie dynamisch mit der CRT verknüpfen, können möglicherweise Code statisch verknüpft werden kann (z. B. `DllMainCRTStartup`).

Wenn Sie Ihr Image verknüpfen, geben Sie entweder explizit oder implizit einen Einstiegspunkt dar, den nach dem Laden des Images des Betriebssystems aufgerufen wird. Für eine DLL ist der Standardeinstiegspunkt `DllMainCRTStartup`. Für eine EXE-Datei, ist es `WinMainCRTStartup`. Sie können die Standardeinstellung mit der Linkeroption/Entry überschreiben. Bietet eine Implementierung für die CRT `DllMainCRTStartup`, `WinMainCRTStartup`, und `wWinMainCRTStartup` (Unicode-Einstiegspunkt für eine EXE-Datei). Diese CRT bereitgestellte Einstiegspunkte Konstruktoren für globale Objekte aufrufen, und initialisieren andere Datenstrukturen, die von einigen CRT-Funktionen verwendet werden. Dieser Startcode hinzugefügt Ihres Images ungefähr 25 KB, wenn es statisch verknüpft ist. Wenn sie dynamisch verknüpft ist, Großteil des Codes ist in der DLL, damit die Größe Ihres Images gering bleibt.

Weitere Informationen finden Sie im Linkerthema [/Entry (Symbol für Einstiegspunkt)](../build/reference/entry-entry-point-symbol.md).

## <a name="optimization-options"></a>Optimierungsoptionen

Die Linkeroption NOWIN98 kann weiter ein standardmäßiges ATL-Steuerelement von 10 K, auf Kosten der reduzieren Ladezeiten bei Windows 98-Systeme. Weitere Informationen zu Optionen zu verknüpfen, finden Sie unter [/OPT (Optimierungen)](../build/reference/opt-optimizations.md).

## <a name="see-also"></a>Siehe auch

[Programmieren mit ATL- und C-Laufzeitcode](../atl/programming-with-atl-and-c-run-time-code.md)<br/>
[DLLs and Visual C++ run-time library behavior (Verhalten der Laufzeitbibliothek für DLLs und Visual C++)](../build/run-time-library-behavior.md)

