---
title: Compilerfehler C2483
ms.date: 09/15/2017
f1_keywords:
- C2483
helpviewer_keywords:
- C2483
ms.assetid: 5762b325-914b-442d-a604-e4617ba04038
ms.openlocfilehash: d1a5632328c00ca2dcd03519d03fbdb648776a51
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50637878"
---
# <a name="compiler-error-c2483"></a>Compilerfehler C2483

>"*Bezeichner*": Objekt mit dem Konstruktor oder Destruktor kann nicht als "thread" deklariert werden

Diese Fehlermeldung ist in Visual Studio 2015 und höher veraltet. In früheren Versionen Variablen deklariert, mit der `thread` Attribut kann nicht initialisiert werden, mit einem Konstruktor oder ein anderer Ausdruck, der Auswertung der Laufzeit erfordert. Ein statischer Ausdruck ist erforderlich, um das Initialisieren `thread` Daten.

## <a name="example"></a>Beispiel

Im folgende Beispiel wird die C2483 generiert in Visual Studio 2013 und früheren Versionen.

```cpp
// C2483.cpp
// compile with: /c
__declspec(thread) struct A {
   A(){}
   ~A(){}
} aa;   // C2483 error

__declspec(thread) struct B {} b;   // OK
```

## <a name="see-also"></a>Siehe auch

[thread](../../cpp/thread.md)