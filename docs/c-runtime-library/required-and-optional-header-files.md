---
title: Erforderliche und optionale Headerdateien
ms.date: 11/04/2016
f1_keywords:
- c.headers
helpviewer_keywords:
- include files, required in run time
- header files, required in run time
ms.assetid: f64d0bf5-e2c3-4b42-97d0-443b3d901d9f
ms.openlocfilehash: db3b05edf1496d92eaed5c7f07b9961cdde351c2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50539411"
---
# <a name="required-and-optional-header-files"></a>Erforderliche und optionale Headerdateien

Die Beschreibung jeder Laufzeitroutine enthält eine Liste der erforderlichen und optionalen Include- oder Headerdateien (.H) für diese Routine. Erforderliche Headerdateien müssen eingeschlossen werden, um die Funktionsdeklaration für die Routine abzurufen, oder eine Definition, die von einer anderen, intern aufgerufenen Routine verwendet wird. Optionale Headerdateien werden in der Regel eingeschlossen, um vordefinierte Konstanten, Typdefinitionen oder Inlinemakros zu nutzen. Die folgende Tabelle enthält einige Beispiele für die Inhalte optionaler Headerdateien:

|Definition|Beispiel|
|----------------|-------------|
|Makrodefinition|Wenn eine Bibliotheksroutine als Makro implementiert wird, kann sich die Makrodefinition in einer anderen Headerdatei als der Headerdatei für die ursprüngliche Routine befinden. Beispielsweise ist das `_toupper`-Makro in der Headerdatei CTYPE.H definiert, die Funktion `toupper` hingegen in STDLIB.H.|
|Vordefinierte Konstante|Viele Bibliotheksroutinen verweisen auf Konstanten, die in Headerdateien definiert sind. Beispielsweise verwendet die `_open`-Routine Konstanten wie z.B. `_O_CREAT`, die in der Headerdatei FCNTL.H definiert ist.|
|Typdefinition|Einige Bibliotheksroutinen geben eine Struktur zurück oder übernehmen eine Struktur als Argument. Routinen zur Datenstromeingabe/-ausgabe verwenden z.B. eine Struktur vom Typ `FILE`, die in STDIO.H definiert ist.|

Die Laufzeitbibliothek-Headerdateien bieten Funktionsdeklarationen im empfohlenen Format des ANSI/ISO-C-Standards. Der Compiler führt eine Typüberprüfung für alle Routinenverweise durch, die nach der zugeordneten Funktionsdeklaration erfolgt. Funktionsdeklarationen sind besonders wichtig für Routinen, die einen Wert eines bestimmten Typs außer `int` zurückgeben; dies ist die Standardeinstellung. Bei Routinen, die den jeweiligen Rückgabewert nicht in ihrer Deklaration angeben, setzt der Compiler die Rückgabe von `int` voraus, was zu unerwarteten Ergebnissen führen kann. Weitere Informationen finden Sie unter [Typüberprüfung](../c-runtime-library/type-checking-crt.md).

## <a name="see-also"></a>Siehe auch

[CRT-Bibliotheksfunktionen](../c-runtime-library/crt-library-features.md)