---
title: Compilerfehler C2427
ms.date: 11/04/2016
f1_keywords:
- C2427
helpviewer_keywords:
- C2427
ms.assetid: a7d421af-6180-40b4-b7a6-9f3bc7dfaaf9
ms.openlocfilehash: b794b90a476f7712c80e7617ec3c0696afb290ec
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50609848"
---
# <a name="compiler-error-c2427"></a>Compilerfehler C2427

'Klasse': in diesem Bereich kann die Klasse nicht definiert

Es wurde versucht, eine geschachtelte Klasse definiert, aber die geschachtelte Klasse ist ein Member einer Basisklasse, die nicht die übergeordnete Klasse.

Im folgende Beispiel wird die C2427 generiert:

```
// C2427.cpp
// compile with: /c
template <class T>
struct S {
   struct Inner;
};

struct Y : S<int> {};

struct Y::Inner {};   // C2427

// OK
template<typename T>
struct S<T>::Inner {};
```