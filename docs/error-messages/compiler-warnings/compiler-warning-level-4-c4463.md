---
title: Compilerwarnung (Stufe 4) C4463 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C4463
dev_langs:
- C++
helpviewer_keywords:
- C4463
ms.assetid: a07ae70c-db4e-472b-8b58-9137d9997323
caps.latest.revision: 0
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 128bd124c2536d86c8b673b54abc4b5505526b41
ms.openlocfilehash: 63f9c9172daffe11f91c521f514f0e8e53331b22
ms.contentlocale: de-de
ms.lasthandoff: 05/10/2017

---
# <a name="compiler-warning-level-4-c4463"></a>Compilerwarnung (Stufe 4) C4463  
  
> Überlauf; Zuweisen von *Wert* Bitfeld, das nur Werte aus enthalten können *Low_value* auf *High_value*  
  
Die zugewiesene *Wert* liegt außerhalb des Bereichs von Werten, die das Bitfeld aufnehmen kann. Typen mit Vorzeichen Bitfeld verwenden die höherwertigen bit für das Zeichen, wenn also  *n*  ist die Größe des Bereichs Bitfeld mit Vorzeichen von Bitfeldern-2<sup>n-1</sup> auf 2<sup>n-1</sup>-1 und zwar ohne Vorzeichen von Bitfeldern einen Bereich von 0 bis 2 aufweisen<sup>n</sup>-1.  
  
## <a name="example"></a>Beispiel  
  
In diesem Beispiel wird C4463 generiert, weil er versucht, einen Wert von 3 auf ein Bitfeld des Typs zuzuweisen `int` mit einer Länge von 2, die über einen Bereich von-2 bis 1 verfügt.  
  
Um dieses Problem zu beheben, können Sie den zugewiesenen Wert auf einen anderen Wert im zulässigen Bereich ändern. Das Bitfeld zum Aufnehmen von Werten ohne Vorzeichen im Bereich von 0 bis 3 vorgesehen ist, können Sie ändern den Deklarationstyp, `unsigned`. Wenn das Feld zum Speichern der Werte in-4 bis 3 Bereich vorgesehen ist, können Sie die Größe der Bitfeld auf 3 ändern.  
  
```cpp  
// C4463_overflow.cpp
// compile with: cl /W4 /EHsc C4463_overflow.cpp
struct S { 
    int x : 2; // int type treats high-order bit as sign
}; 

int main() { 
    S s; 
    s.x = 3; // warning C4463: overflow; assigning 3 
    // to bit-field that can only hold values from -2 to 1 
    // To fix, change assigned value to fit in range,
    // increase size of bitfield, and/or change base type 
    // to unsigned.
} 
```  
