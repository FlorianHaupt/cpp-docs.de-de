---
title: Compilerfehler C3872
ms.date: 11/04/2016
f1_keywords:
- C3872
helpviewer_keywords:
- C3872
ms.assetid: 519e95be-5641-40cc-894c-da4819506604
ms.openlocfilehash: 5cadb8165b5b63b2f7ac2d4cc31e2623b0f6bce9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50649893"
---
# <a name="compiler-error-c3872"></a>Compilerfehler C3872

„char“: Dieses Zeichen ist in einem Bezeichner nicht zulässig.

Der C++-Compiler folgt hinsichtlich Zeichen, die in einem Bezeichner zulässig sind, dem C++11-Standard. Nur bestimmte Bereiche von Zeichen und universelle Zeichennamen sind in einem Bezeichner zulässig. Zusätzliche Einschränkungen gelten für das erste Zeichen eines Bezeichners. Weitere Informationen hierzu und eine Liste der zulässigen Zeichen sowie Bereiche universeller Zeichennamen finden Sie unter [Identifiers](../../cpp/identifiers-cpp.md).

Der Bereich der in einem Bezeichner zulässigen Zeichen ist weniger restriktiv, wenn C++ /CLI-Code kompiliert wird. Bezeichner in Code, der mit „/clr“ kompiliert wurde, müssen dem folgenden Standard entsprechen:  [Standard ECMA-335: Common Language Infrastructure (CLI)](http://www.ecma-international.org/publications/standards/Ecma-335.htm).

Im folgenden Beispiel wird C3872 generiert:

```
// C3872.cpp
int main() {
   int abc_\u0040;   // C3872, U+0040 is in base char set
   int abc_\u3001;   // C3872, U+3001 is not in allowed range
   int \u30A2_abc_\u3042;   // OK, UCNs in allowed range
}
```