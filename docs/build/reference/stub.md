---
title: STUB
ms.date: 11/04/2016
f1_keywords:
- STUB
helpviewer_keywords:
- STUB .def file statement
ms.assetid: 0a3b9643-19ed-47e9-8173-ee16bc8ed056
ms.openlocfilehash: 95f8e1584bdd87f23e87c27418c0debca5c3181a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50533717"
---
# <a name="stub"></a>STUB

Wenn eine Moduldefinitionsdatei verwendet, die einen virtuellen Gerätetreiber (VxD) erstellt, können Sie einen Dateinamen angeben, der eine Anweisung-Struktur (definiert in WINNT. enthält H), die im virtuellen Gerätetreiber (VxD), statt der Standardheader verwendet werden.

```
STUB:filename
```

## <a name="remarks"></a>Hinweise

Eine entsprechende Möglichkeit zum angeben *Filename* ist mit der [/STUB](../../build/reference/stub-ms-dos-stub-file-name.md) -Linkeroption.

STUB gilt in eine Moduldefinitionsdatei, nur, wenn Sie einen VxD zu erstellen.

## <a name="see-also"></a>Siehe auch

[Regeln für Moduldefinitionsanweisungen](../../build/reference/rules-for-module-definition-statements.md)