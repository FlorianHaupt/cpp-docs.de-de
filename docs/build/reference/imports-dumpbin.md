---
title: /IMPORTS (DUMPBIN)
ms.date: 11/04/2016
f1_keywords:
- /imports
helpviewer_keywords:
- IMPORTS dumpbin option
- /IMPORTS dumpbin option
- -IMPORTS dumpbin option
ms.assetid: 6a296216-2b1b-40f8-8736-cd4553a22456
ms.openlocfilehash: 9367457a8e7f6be1f372244f8288a994eb777071
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50613784"
---
# <a name="imports-dumpbin"></a>/IMPORTS (DUMPBIN)

```
/IMPORTS[:file]
```

Diese Option zeigt die Liste der DLLs (sowohl die statisch verknüpfte und [verzögert geladene](../../build/reference/linker-support-for-delay-loaded-dlls.md)), die in eine ausführbare Datei oder DLL und alle einzelnen Importe aus jeder dieser DLLs importiert werden.

Der optionale `file` Spezifikation können Sie angeben, dass die Importe nur diese DLL angezeigt werden. Zum Beispiel:

```
dumpbin /IMPORTS:msvcrt.dll
```

## <a name="remarks"></a>Hinweise

Die Ausgabe angezeigt, die durch diese Option ist vergleichbar mit der [/EXPORTS](../../build/reference/dash-exports.md) Ausgabe.

Nur die [/Headers](../../build/reference/headers.md) DUMPBIN-Option ist verfügbar für die Verwendung in Dateien mit der ["/ GL"](../../build/reference/gl-whole-program-optimization.md) -Compileroption.

## <a name="see-also"></a>Siehe auch

[DUMPBIN-Optionen](../../build/reference/dumpbin-options.md)