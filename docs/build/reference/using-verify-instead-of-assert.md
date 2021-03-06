---
title: Verwenden von VERIFY anstelle ASSERT
ms.date: 11/04/2016
f1_keywords:
- assert
helpviewer_keywords:
- ASSERT statements
- debugging [MFC], ASSERT statements
- VERIFY macro
- assertions, troubleshooting ASSERT statements
- debugging assertions
- assertions, debugging
ms.assetid: 4c46397b-3fb1-49c1-a09b-41a72fae3797
ms.openlocfilehash: 266c6da52a2ff5e06dd6177a746c22e7df5adda4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50491779"
---
# <a name="using-verify-instead-of-assert"></a>Verwenden von VERIFY anstelle ASSERT

Nehmen wir an, wenn Sie die Debugversion der MFC-Anwendung ausführen, gibt es keine Probleme vorliegen. Die Releaseversion einer Anwendung allerdings stürzt ab, gibt falsche Ergebnisse zurück und/oder weist einige andere ungewöhnliches Verhalten.

Dieses Problem kann verursacht werden, wenn Sie wichtigsten Code, in einer ASSERT-Anweisung einfügen, um sicherzustellen, dass es ordnungsgemäß funktioniert. Da die ASSERT-Anweisungen in einem Releasebuild von einem MFC-Programm auskommentiert werden, wird der Code nicht in einem Releasebuild ausgeführt.

Wenn Sie ASSERT zu verwenden, um zu bestätigen, dass ein Funktionsaufruf erfolgreich war, sollten Sie verwenden [überprüfen](../../mfc/reference/diagnostic-services.md#verify) stattdessen. VERIFY-Makro wertet seine eigenen Argumente in sowohl für Debug- und Releasebuilds der Anwendung.

Eine weitere bevorzugte Methode besteht darin, eine temporäre Variable der Funktion zurückgegebene Wert zuweisen, und klicken Sie dann testen Sie die Variable in einer ASSERT-Anweisung.

Überprüfen Sie das folgende Codefragment:

```
enum {
    sizeOfBuffer = 20
};
char *buf;
ASSERT(buf = (char *) calloc(sizeOfBuffer, sizeof(char) ));
strcpy_s( buf, sizeOfBuffer, "Hello, World" );
free( buf );
```

Dieser Code, die perfekt in einer Debugversion der MFC-Anwendung ausgeführt wird. Wenn der Aufruf von `calloc( )` ein Fehler auftritt, wird angezeigt, eine diagnosemeldung aus, die die Anzahl und die Zeilennummer enthält. Allerdings in einer Verkaufsversion einer MFC-Anwendung:

- der Aufruf von `calloc( )` nie auftritt, sodass `buf` nicht initialisiert ist, oder

- `strcpy_s( )` Kopien "`Hello, World`" an eine beliebige Stelle des Arbeitsspeichers, möglicherweise die Anwendung abstürzt, oder dass das System nicht mehr reagiert, oder

- `free()` versucht, Speicherplatz freizugeben, der nie zugeordnet wurde.

Um ASSERT ordnungsgemäß zu verwenden, sollte das Codebeispiel folgt geändert werden:

```
enum {
    sizeOfBuffer = 20
};
char *buf;
buf = (char *) calloc(sizeOfBuffer, sizeof(char) );
ASSERT( buf != NULL );
strcpy_s( buf, sizeOfBuffer, "Hello, World" );
free( buf );
```

Alternativ können Sie stattdessen stellen Sie sicher verwenden:

```
enum {
    sizeOfBuffer = 20
};
char *buf;
VERIFY(buf = (char *) calloc(sizeOfBuffer, sizeof(char) ));
strcpy_s( buf, sizeOfBuffer, "Hello, World" );
free( buf );
```

## <a name="see-also"></a>Siehe auch

[Beheben von Problemen mit dem Releasebuild](../../build/reference/fixing-release-build-problems.md)