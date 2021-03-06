---
title: 3.1.9 omp_set_nested-Funktion
ms.date: 11/04/2016
ms.assetid: e4afc3aa-bb96-4314-9849-fd5df5f437d9
ms.openlocfilehash: 683c2cf684aa7212b8323fda9f748812fa9c3359
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50648005"
---
# <a name="319-ompsetnested-function"></a>3.1.9 omp_set_nested-Funktion

Die **Omp_set_nested** Funktion aktiviert oder deaktiviert den geschachtelten Parallelität. Es wird folgendes Format verwendet:

```
#include <omp.h>
void omp_set_nested(int nested);
```

Wenn *geschachtelte* auf 0 (null) und geschachtelten wertet Parallelität deaktiviert ist, dies ist die Standardeinstellung und geschachtelten parallele Bereichen werden serialisiert und von den aktuellen Thread ausgeführt werden. Wenn *geschachtelte* ergibt einen Wert ungleich NULL, geschachtelte Parallelität aktiviert ist und parallele Bereichen, die geschachtelt sind möglicherweise zusätzliche Threads um geschachtelte Teams zu bilden bereitstellen.

Diese Funktion hat die Auswirkungen, die oben beschriebenen, beim Aufrufen durch einen Teil des Programms, in denen die **Omp_in_parallel** Funktion gibt 0 (null) zurück. Wenn sie über einen Teil des Programms aufgerufen wird, in denen die **Omp_in_parallel** Funktion gibt einen Wert ungleich NULL zurück, das Verhalten dieser Funktion ist nicht definiert.

Dieser Aufruf hat Vorrang vor den **OMP_NESTED** -Umgebungsvariablen angegeben.

Wenn geschachtelte Parallelität aktiviert ist, wird die Anzahl der Threads, die zum Ausführen von geschachtelten paralleler Bereichen verwendet die Implementierung definiert. Daher dürfen OpenMP konforme Implementierungen geschachtelten parallele Bereichen zu serialisieren, auch wenn geschachtelte Parallelität aktiviert ist.

## <a name="cross-references"></a>Datenbankübergreifende Verweise:

- **OMP_NESTED** Umgebung Variablen, finden Sie unter [Abschnitt 4.4](../../parallel/openmp/4-4-omp-nested.md) auf 49.

- **Omp_in_parallel** funktionieren, finden Sie unter [Abschnitt 3.1.6](../../parallel/openmp/3-1-6-omp-in-parallel-function.md) auf 38.