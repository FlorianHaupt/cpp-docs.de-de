---
title: Compilerfehler C2989
ms.date: 11/04/2016
f1_keywords:
- C2989
helpviewer_keywords:
- C2989
ms.assetid: 936303d8-eb3b-4746-82ec-2f18020a6f64
ms.openlocfilehash: e5f03d644ab6c25b7eb0da0dc1684c7de5c2e6a8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50517896"
---
# <a name="compiler-error-c2989"></a>Compilerfehler C2989

'Klasse': Klassentyp wurde bereits als Nichtklassen-Typ deklariert

Die generische oder Vorlagenklasse definiert eine Klasse ohne Vorlagen oder nicht generisch. Überprüfen Sie die Headerdateien für Konflikte.

Im folgende Beispiel wird die C2989 generiert:

```cpp
// C2989.cpp
// compile with: /c
class C{};

template <class T>
class C{};  // C2989
class C2{};
```

C2989 kann auch auftreten, wenn Generika verwendet werden:

```cpp
// C2989b.cpp
// compile with: /clr /c
ref class GC1;

generic <typename T> ref class GC1;   // C2989
template <typename T> ref class GC2;

generic <typename T> ref class GC2;   // C2989
generic <typename T> ref class GCb;
template <typename T> ref class GC2;
generic <typename T> ref class GCc;
```