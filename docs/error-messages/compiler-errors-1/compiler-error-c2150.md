---
title: Compilerfehler C2150
ms.date: 11/04/2016
f1_keywords:
- C2150
helpviewer_keywords:
- C2150
ms.assetid: 21e82a10-c1d4-4c0d-9dc6-c5d92ea42a31
ms.openlocfilehash: a9c6465ef87c12135ad4e6709741f0027d8ea3c7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50638190"
---
# <a name="compiler-error-c2150"></a>Compilerfehler C2150

> "*Bezeichner*": Bitfeld muss vom Typ 'Int','signed Int' oder 'unsigned Int' aufweisen

Der Basistyp für Bitfeld ist erforderlich, um werden `int`, `signed int`, oder `unsigned int`.

## <a name="example"></a>Beispiel

In diesem Beispiel wird gezeigt, wie C2150 auftreten können und wie Sie es beheben können:

```cpp
// C2150.cpp
// compile with: /c
struct A {
   float a : 8;    // C2150
   int i : 8;      // OK
};
```