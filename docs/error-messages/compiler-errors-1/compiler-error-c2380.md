---
title: Compilerfehler C2380
ms.date: 11/04/2016
f1_keywords:
- C2380
helpviewer_keywords:
- C2380
ms.assetid: 717b1e6e-ddfe-4bac-a5f3-7f9a4dcb1572
ms.openlocfilehash: c0494d4ba405a084e7b455139016c98af7d95191
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50584495"
---
# <a name="compiler-error-c2380"></a>Compilerfehler C2380

Typ(en) vor 'Bezeichner'-Konstruktor mit Ergebnistyp oder unzulässige Neudefinition eines Klassennamens?

Ein Konstruktor gibt einen Wert zurück, oder den Namen der Klasse definiert.

Im folgenden Beispiel wird C2326 generiert:

```
// C2380.cpp
// compile with: /c
class C {
public:
   int C();   // C2380, specifies an int return
   int C;   // C2380, redefinition of i
   C();   // OK
};
```