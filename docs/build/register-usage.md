---
title: Registerverwendung
ms.date: 11/04/2016
ms.assetid: ce58e2cf-afd3-4068-980e-28a209298265
ms.openlocfilehash: fa04318ad4af298f300fbbbad8c01d0df9500ec7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50629982"
---
# <a name="register-usage"></a>Registerverwendung

Die Architektur bietet für 16 allgemeinen Registern (im folgenden als Ganzzahl-Register bezeichnet) sowie von 16 XMM/YMM X64 registriert Gleitkommaregister zur Verfügung. Volatile Register sind Scratch-Register, von denen der Aufrufer voraussetzt, dass sie während eines Aufrufs zerstört werden. Nicht volatile Register müssen ihre Werte über einen Funktionsaufruf hinweg bewahren und, sofern sie verwendet werden, vom Aufgerufenen gespeichert werden.

## <a name="register-volatility-and-preservation"></a>Gibt die Volatilität und Beibehaltung der registrieren

Die folgende Tabelle beschreibt, wie jedes Register bei Funktionsaufrufen verwendet wird:

||||
|-|-|-|
|Register|Status|Verwendung|
|RAX|Volatil|Rückgabewert-Register|
|RCX|Volatil|Erstes Ganzzahl-Argument|
|RDX|Volatil|Zweites Ganzzahl-Argument|
|R8|Volatil|Drittes Ganzzahl-Argument|
|R9|Volatil|Viertes Ganzzahl-Argument|
|R10:R11|Volatil|Muss je nach Anforderung des Aufrufers bewahrt werden. Wird in syscall-/sysret-Instruktionen verwendet.|
|R12:R15|Nicht volatil|Muss vom Aufgerufenen bewahrt werden|
|RDI|Nicht volatil|Muss vom Aufgerufenen bewahrt werden|
|RSI|Nicht volatil|Muss vom Aufgerufenen bewahrt werden|
|RBX|Nicht volatil|Muss vom Aufgerufenen bewahrt werden|
|RBP|Nicht volatil|Kann als Frame-Pointer verwendet werden; muss vom Aufgerufenen bewahrt werden|
|RSP|Nicht volatil|Stack-Pointer|
|XMM0, YMM0|Volatil|Erstes FP-Argument; erstes Argument vom Typ Vektor, wenn `__vectorcall` verwendet wird|
|XMM1, YMM1|Volatil|Zweites FP-Argument; zweites Argument vom Typ Vektor, wenn `__vectorcall` verwendet wird|
|XMM2, YMM2|Volatil|Drittes FP-Argument; drittes Argument vom Typ Vektor, wenn `__vectorcall` verwendet wird|
|XMM3, YMM3|Volatil|Viertes FP-Argument; viertes Argument vom Typ Vektor, wenn `__vectorcall` verwendet wird|
|XMM4, YMM4|Volatil|Muss je nach Bedarf vom Aufrufer bewahrt werden; fünftes Argument vom Typ Vektor, wenn `__vectorcall` verwendet wird|
|XMM5, YMM5|Volatil|Muss je nach Bedarf vom Aufrufer bewahrt werden; sechstes Argument vom Typ Vektor, wenn `__vectorcall` verwendet wird|
|XMM6:XMM15, YMM6:YMM15|Nicht volatil (XMM), Volatil (obere Hälfte von YMM)|Muss vom aufgerufenen bewahrt werden. YMM-Register müssen je nach Bedarf vom Aufrufer bewahrt werden.|

Bei Funktionsende und Funktion-Eintrags, der C-Laufzeitbibliothek-Aufrufe und Aufrufe der Windows-System, das Richtungsflag in der CPU Flags registrieren soll gelöscht werden.

## <a name="see-also"></a>Siehe auch

- [x64-Softwarekonventionen](../build/x64-software-conventions.md)
- [__vectorcall](../cpp/vectorcall.md)
- [Richtungsflag](../c-runtime-library/direction-flag.md)
