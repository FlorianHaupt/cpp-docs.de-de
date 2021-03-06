---
title: 3.1.1 omp_set_num_threads-Funktion
ms.date: 11/04/2016
ms.assetid: b94cf2b5-8011-4a3b-ba56-676982642857
ms.openlocfilehash: 20b6b6ced2b4031696f1d019604842ae9b91bda2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50663280"
---
# <a name="311-ompsetnumthreads-function"></a>3.1.1 omp_set_num_threads-Funktion

Die `omp_set_num_threads` -Funktion legt fest, die Standardanzahl von Threads an, für nachfolgende parallelen Bereichen verwendet, die keine angeben einer `num_threads` Klausel. Es wird folgendes Format verwendet:

```
#include <omp.h>
void omp_set_num_threads(int num_threads);
```

Der Wert des Parameters *Num_threads* muss eine positive ganze Zahl sein. Die Auswirkungen hängt davon ab, ob die dynamische Anpassung der Anzahl der Threads aktiviert ist. Für einen umfassenden Satz von Regeln über die Interaktion zwischen der `omp_set_num_threads` -Funktion und die dynamische Anpassung der Threads finden Sie in Abschnitt 2.3 auf der Seite 8.

Diese Funktion hat die Auswirkungen, die oben beschriebenen, beim Aufrufen durch einen Teil des Programms, in denen die `omp_in_parallel` Funktion gibt 0 (null) zurück. Wenn sie über einen Teil des Programms aufgerufen wird, in denen die `omp_in_parallel` Funktion gibt einen Wert ungleich NULL zurück, das Verhalten dieser Funktion ist nicht definiert.

Dieser Aufruf hat Vorrang vor den `OMP_NUM_THREADS` -Umgebungsvariablen angegeben. Der Standardwert für die Anzahl der Threads, die durch den Aufruf festgelegt werden kann `omp_set_num_threads` oder durch Festlegen der `OMP_NUM_THREADS` Umgebungsvariable kann auf einem einzelnen explizit überschrieben werden **parallele** -Anweisung durch Angabe der `num_threads` Klausel.

## <a name="cross-references"></a>Datenbankübergreifende Verweise:

- `omp_set_dynamic` funktionieren, finden Sie unter [Abschnitt 3.1.7](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) auf Seite 39.

- `omp_get_dynamic` funktionieren, finden Sie unter [Abschnitt 3.1.8](../../parallel/openmp/3-1-8-omp-get-dynamic-function.md) auf Seite "40".

- `OMP_NUM_THREADS` Umgebung-Variable, finden Sie unter [Abschnitt 4.2](../../parallel/openmp/4-2-omp-num-threads.md) auf Seite 48 und Abschnitt 2.3 auf 8.

- `num_threads` -Klausel finden Sie unter [Abschnitt 2.3](../../parallel/openmp/2-3-parallel-construct.md) auf Seite 8