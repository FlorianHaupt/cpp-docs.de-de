---
title: Compilerwarnung (Stufe 1) C4551
ms.date: 11/04/2016
f1_keywords:
- C4551
helpviewer_keywords:
- C4551
ms.assetid: 458b59bd-e2d7-425f-9ba6-268ff200424f
ms.openlocfilehash: 8a30ad5622d8e889a7f3ec64b73ead7c63f65b48
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50616821"
---
# <a name="compiler-warning-level-1-c4551"></a>Compilerwarnung (Stufe 1) C4551

die Argumentliste der Funktion Aufruf fehlt

Ein Funktionsaufruf muss die öffnen und schließen Klammern nach dem Funktionsnamen enthalten, selbst wenn die Funktion keine Parameter akzeptiert.

Im folgende Beispiel wird die C4551 generiert:

```
// C4551.cpp
// compile with: /W1
void function1() {
}

int main() {
   function1;   // C4551
   function1();   // OK
}
```