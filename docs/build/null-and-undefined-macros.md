---
title: NULL-Makros und undefinierte Makros
ms.date: 11/04/2016
helpviewer_keywords:
- NMAKE program, undefined macros
- Null macros in NMAKE
- macros, null and undefined
- undefined macros and NMAKE
- NMAKE program, null macros
ms.assetid: 1db4611a-1755-4328-b00f-d35365af8b6c
ms.openlocfilehash: f6f294234f7244b65137742e1fe8abaa37a676a5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50498916"
---
# <a name="null-and-undefined-macros"></a>NULL-Makros und undefinierte Makros

Null und Undefinierte Makros erweitern, um null-Zeichenfolgen, aber ein Makro definiert als null-Zeichenfolge gelten als definiert, in der Vorabverarbeitung von Ausdrücken. Geben Sie zum Definieren eines Makros als null-Zeichenfolge keine Zeichen außer Leerzeichen oder Tabstopps hinter dem Gleichheitszeichen (=) in einer Befehlszeile oder Befehlsdatei, und schließen Sie die null-Zeichenfolge oder der Definition in doppelte Anführungszeichen (""). Um ein Makro aufzuheben, verwenden Sie **! UNDEF.** Weitere Informationen finden Sie unter [Direktiven für die Makefile-Vorverarbeitung](../build/makefile-preprocessing-directives.md).

## <a name="see-also"></a>Siehe auch

[Definieren eines NMAKE-Makros](../build/defining-an-nmake-macro.md)