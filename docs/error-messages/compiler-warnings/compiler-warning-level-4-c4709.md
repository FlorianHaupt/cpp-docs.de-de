---
title: Compilerwarnung (Stufe 4) C4709
ms.date: 11/04/2016
f1_keywords:
- C4709
helpviewer_keywords:
- C4709
ms.assetid: 8abfdd45-8c70-4c27-b0fb-ca0c3f0fccf9
ms.openlocfilehash: acc74f55a423f1cd18d385cd4dfbec7dfa01c422
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50536105"
---
# <a name="compiler-warning-level-4-c4709"></a>Compilerwarnung (Stufe 4) C4709

Kommaoperator innerhalb eines Feldindex-Ausdrucks

Tritt ein Komma in einem Feldindex-Ausdrucks, verwendet der Compiler den Wert nach dem letzten Komma.

## <a name="example"></a>Beispiel

Im folgende Beispiel wird die C4709 generiert:

```
// C4709.cpp
// compile with: /W4
#include <stdio.h>

int main()
{
    int arr[2][2];
    arr[0][0] = 10;
    arr[0][1] = 11;

    // Prints 10, not 11
    printf_s("\n%d",arr[0][1,0]);   // C4709
}
```