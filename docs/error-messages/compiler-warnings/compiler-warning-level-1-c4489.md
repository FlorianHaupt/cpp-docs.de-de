---
title: Compilerwarnung (Stufe 1) C4489
ms.date: 11/04/2016
f1_keywords:
- C4489
helpviewer_keywords:
- C4489
ms.assetid: 43b51c8c-27b5-44c9-b974-fe4b48f4896f
ms.openlocfilehash: 4da96fd13fe9ba03c19808d32d3cdd9c73ec2b18
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50584729"
---
# <a name="compiler-warning-level-1-c4489"></a>Compilerwarnung (Stufe 1) C4489

"Spezifizierer": nicht zulässig für Schnittstellenmethode 'Methode'; Überschreiben Sie Bezeichner sind nur für Ref-Klasse und Werteklassenmethoden zulässig

Ein Bezeichner-Schlüsselwort wurde falsch auf Schnittstellenmethoden verwendet.

Weitere Informationen finden Sie unter [Überschreibungsspezifizierer](../../windows/override-specifiers-cpp-component-extensions.md).

## <a name="example"></a>Beispiel

Im folgende Beispiel wird die C4489 generiert.

```
// C4489.cpp
// compile with: /clr /c /W1
public interface class I {
   void f() new;   // C4489
   virtual void b() override;   // C4489

   void g();   // OK
};
```