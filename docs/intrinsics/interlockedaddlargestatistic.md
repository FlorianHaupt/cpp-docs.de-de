---
title: _InterlockedAddLargeStatistic
ms.date: 11/04/2016
f1_keywords:
- _InterlockedAddLargeStatistic
- _InterlockedAddLargeStatistic_cpp
helpviewer_keywords:
- _InterlockedAddLargeStatistic intrinsic
- InterlockedAddLargeStatistic intrinsic
ms.assetid: 2802e74b-bcee-46e4-b562-894908d44409
ms.openlocfilehash: befcd74c432eb62ab3a718223ada6d0f441e72c0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50432824"
---
# <a name="interlockedaddlargestatistic"></a>_InterlockedAddLargeStatistic

**Microsoft-spezifisch**

Führt eine ineinander greifende Addition, in der der erste Operand ein 64-Bit-Wert ist.

## <a name="syntax"></a>Syntax

```
long _InterlockedAddLargeStatistic(
   __int64 volatile * Addend,
   long Value
);
```

#### <a name="parameters"></a>Parameter

*Addend*<br/>
[in, out] Ein Zeiger auf den ersten Operanden, der Vorgang zum Hinzufügen. Der Wert, der auf den verwiesen wird, wird durch das Ergebnis der Addition ersetzt.

*Wert*<br/>
[in] Der zweite Operand; Wert, der erste Operand hinzugefügt.

## <a name="return-value"></a>Rückgabewert

Der Wert des zweiten Operanden.

## <a name="requirements"></a>Anforderungen

|Systemintern|Architektur|
|---------------|------------------|
|`_InterlockedAddLargeStatistic`|x86|

**Headerdatei** \<intrin.h >

## <a name="remarks"></a>Hinweise

Diese systeminterne Funktion ist nicht unteilbar, da er implementiert wird, wenn zwei gesperrte Anweisungen trennen. Ein atomic 64-Bit-Lesevorgang, die in einem anderen Thread während der Ausführung dieser Funktion tritt auf, verursachen in einem inkonsistenten Wert gelesen wird.

Diese Funktion verhält sich wie eine Barriere Lese-/ Schreibzugriff. Weitere Informationen finden Sie unter [ReadWriteBarrier](../intrinsics/readwritebarrier.md).

**Ende Microsoft-spezifisch**

## <a name="see-also"></a>Siehe auch

[Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)<br/>
[Konflikt mit dem x86-Compiler](../build/conflicts-with-the-x86-compiler.md)