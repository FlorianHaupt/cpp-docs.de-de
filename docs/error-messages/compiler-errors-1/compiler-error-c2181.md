---
title: Compilerfehler C2181
ms.date: 11/04/2016
f1_keywords:
- C2181
helpviewer_keywords:
- C2181
ms.assetid: d52b2fe4-566a-40a9-b8e2-8dce1f287668
ms.openlocfilehash: a676794b5dedd17cfb973de36d3771ef1130a786
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50527308"
---
# <a name="compiler-error-c2181"></a>Compilerfehler C2181

Ungültiges "else" ohne zugehöriges "if"

Zu jedem `else` -Element muss ein zugehöriges `if`-Element vorhanden sein.

Im folgenden Beispiel wird C2181 generiert:

```
// C2181.cpp
int main() {
   int i = 0;
   else   // C2181
      i = 1;
}
```

Mögliche Lösung:

```
// C2181b.cpp
int main() {
   int i = 0;
   if(i)
      i = 0;
   else
      i = 1;
}
```