---
title: Compilerfehler C2628
ms.date: 11/04/2016
f1_keywords:
- C2628
helpviewer_keywords:
- C2628
ms.assetid: 19a25e77-d5be-4107-88d5-0745b6281f98
ms.openlocfilehash: 90df41ba8ae85e57e40848f8b50f4c1df7c7b541
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50664944"
---
# <a name="compiler-error-c2628"></a>Compilerfehler C2628

"Typ1", gefolgt von "Typ2" ist nicht zulässig (haben Sie vergessen ein ';'?)

Möglicherweise fehlt ein Semikolon.

Im folgende Beispiel wird die C2628 generiert:

```
// C2628.cpp
class CMyClass {}
int main(){}   // C2628 error
```

Mögliche Lösung:

```
// C2628b.cpp
class CMyClass {};
int main(){}
```