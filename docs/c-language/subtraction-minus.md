---
title: Subtraction (-)
ms.date: 11/04/2016
helpviewer_keywords:
- operators [C], subtraction
- subtraction operator, syntax
ms.assetid: 9cacba7d-20b3-4372-8a63-ba5d8ee64177
ms.openlocfilehash: 369096025a67c67775584928d1ee3264a5a10d94
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50480053"
---
# <a name="subtraction--"></a>Subtraction (-)

Der Subtraktionsoperator (**-**) subtrahiert den zweiten Operanden vom ersten. Beide Operanden können entweder vom Typ „Ganze Zahl“ oder „Gleitkommazahl“ sein, oder ein Operand kann ein Zeiger und der andere eine ganze Zahl sein.

Wenn zwei Zeiger subtrahiert werden, wird die Differenz in einen ganzzahligen Wert mit Vorzeichen konvertiert, indem die Differenz durch die Größe eines Werts vom Typ geteilt wird, auf den die Zeiger zeigen. Die Größe des Integralwerts wird durch den Typ **ptrdiff_t** in der Standardincludedatei „stddef.h“ definiert. Das Ergebnis zeigt die Anzahl von Arbeitsspeicherpositionen dieses Typs zwischen den beiden Adressen. Das Ergebnis ist nur für zwei Elemente desselben Arrays garantiert sinnvoll, wie in [Zeigerarithmetik](../c-language/pointer-arithmetic.md) erläutert.

Wenn ein ganzzahliger Wert von einem Zeigerwert subtrahiert wird, konvertiert der Subtraktionsoperator den ganzzahligen Wert (*i*), indem er ihn mit der Größe des Werts multipliziert, auf den der Zeiger zeigt. Nach der Konvertierung stellt der ganzzahlige Wert *i* Arbeitsspeicherpositionen dar, wobei jede Position über die Länge verfügt, die vom Zeigertyp angegeben wird. Wenn der konvertierte ganzzahlige Wert vom Zeigerwert subtrahiert wird, ist das Ergebnis die Speicheradresse *i* Positionen vor der ursprünglichen Adresse. Der neue Zeiger zeigt auf einen Wert von dem Typ, der vom ursprünglichen Zeigerwert angegeben wurde.

## <a name="see-also"></a>Siehe auch

[C-Operatoren (additiv)](../c-language/c-additive-operators.md)