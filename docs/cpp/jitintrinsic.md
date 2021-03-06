---
title: jitintrinsic
ms.date: 11/04/2016
f1_keywords:
- jitintrinsic
- jitintrinsic_cpp
helpviewer_keywords:
- __declspec keyword [C++], jitintrinsic
- jitintrinsic __declspec modifier
ms.assetid: 23dbe416-7ef6-442b-b16d-9a81aab04fa6
ms.openlocfilehash: 9e726413f0bbfbd9d6affa348777c995c51283a5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50519300"
---
# <a name="jitintrinsic"></a>jitintrinsic

Markiert die Funktion als signifikant bei der 64-Bit-Common Language Runtime. Dies wird in bestimmten Funktionen in von Microsoft bereitgestellten Bibliotheken verwendet.

## <a name="syntax"></a>Syntax

```
__declspec(jitintrinsic)
```

## <a name="remarks"></a>Hinweise

**Jitintrinsic** Fügt ein MODOPT (<xref:System.Runtime.CompilerServices.IsJitIntrinsic>) zu einer Funktionssignatur.

Benutzer sind nicht empfehlenswert, von der Verwendung dieses **__declspec** Modifizierer verwenden, da unerwartete Ergebnisse möglich.

## <a name="see-also"></a>Siehe auch

[__declspec](../cpp/declspec.md)<br/>
[Schlüsselwörter](../cpp/keywords-cpp.md)