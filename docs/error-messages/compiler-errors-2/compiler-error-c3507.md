---
title: Compilerfehler C3507
ms.date: 11/04/2016
f1_keywords:
- C3507
helpviewer_keywords:
- C3507
ms.assetid: 75f89767-f6f9-40f6-9820-81a49e09abdf
ms.openlocfilehash: 731e84955192688a87c020b2b65a80ab5671cad6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50648278"
---
# <a name="compiler-error-c3507"></a>Compilerfehler C3507

eine ProgID kann nicht mehr als 39 Zeichen 'Id'; haben. darf keine Zeichensetzung außer '.'; mit einer Ziffer beginnen

Die [progid](../../windows/progid.md) Attribut gelten Einschränkungen für die Werte, die sie nutzen kann.

Im folgende Beispiel wird die C3507 generiert:

```
// C3507.cpp
[module(name="x")];
[
coclass,
progid("0123456789012345678901234567890123456789"),
uuid("00000000-0000-0000-0000-000000000001") // C3507 expected
]
struct CMyStruct {
};
int main() {
}
```