---
title: Compilerfehler C3418
ms.date: 11/04/2016
f1_keywords:
- C3418
helpviewer_keywords:
- C3418
ms.assetid: 54042c04-3c45-41c1-bad7-90f9ee05a21b
ms.openlocfilehash: 8456e9b17b72cd4ac98349d2f2871a1c59f56911
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50482770"
---
# <a name="compiler-error-c3418"></a>Compilerfehler C3418

Der Zugriffsspezifizierer "Spezifizierer" wird nicht unterstützt.

Ein CLR-Zugriffsspezifizierer wurde falsch angegeben.  Weitere Informationen finden Sie unter typsichtbarkeit und membersichtbarkeit in [wie: definieren und Verarbeiten von Klassen und Strukturen (C++ / CLI)](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md).

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird C3418 generiert:

```cpp
// C3418.cpp
// compile with: /clr /c
ref struct m {
internal public:   // C3418
   void test(){}
};

ref struct n {
internal:   // OK
   void test(){}
};
```