---
title: Compilerfehler C3181
ms.date: 11/04/2016
f1_keywords:
- C3181
helpviewer_keywords:
- C3181
ms.assetid: 5d450f8b-6cef-4452-a0c4-2076e967451d
ms.openlocfilehash: b37b28b4332b46aaaf803f58090a72c25e83f47f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50587758"
---
# <a name="compiler-error-c3181"></a>Compilerfehler C3181

'Typ': Ungültiger Operand für den Operator

Ein ungültiger Parameter wurde übergeben, um die [Typeid](../../windows/typeid-cpp-component-extensions.md) Operator. Der Parameter muss es sich um einen verwalteten Typ sein.

Beachten Sie, dass der Compiler Aliase für systemeigene Typen verwendet werden, die Typen in der common Language Runtime zugeordnet.

Im folgende Beispiel wird die C3181 generiert:

```
// C3181a.cpp
// compile with: /clr
using namespace System;

int main() {
   Type ^pType1 = interior_ptr<int>::typeid;   // C3181
   Type ^pType2 = int::typeid;   // OK
}
```
