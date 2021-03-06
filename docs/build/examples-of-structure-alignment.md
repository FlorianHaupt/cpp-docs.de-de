---
title: Beispiele für die Strukturausrichtung
ms.date: 11/19/2018
helpviewer_keywords:
- structure alignment
- examples [C++], structure alignment
ms.assetid: 03d137bf-5cc4-472e-9583-6498f2534199
ms.openlocfilehash: 7c4b3ae29674e9c4fc27e8e175867339001b9a0d
ms.sourcegitcommit: 9e891eb17b73d98f9086d9d4bfe9ca50415d9a37
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2018
ms.locfileid: "52175339"
---
# <a name="examples-of-structure-alignment"></a>Beispiele für die Strukturausrichtung

Die folgenden vier Beispielen wird jeweils deklarieren, dass eine ausgerichtete Struktur oder Union und die entsprechenden Zahlen veranschaulichen das Layout der Struktur oder Union im Arbeitsspeicher. Jede Spalte in einer Abbildung stellt ein Byte Arbeitsspeicher und die Anzahl in der Spalte gibt an, die Verschiebung dieser Bytes. Der Name in der zweiten Zeile von jeder Abbildung entspricht dem Namen einer Variablen in der Deklaration. Die schattierten Spalten anzugeben, dass die Auffüllung, die erforderlich ist, um die angegebene Ausrichtung zu erzielen.

## <a name="example-1"></a>Beispiel 1

```C
// Total size = 2 bytes, alignment = 2 bytes (word).

_declspec(align(2)) struct {
    short a;      // +0; size = 2 bytes
}
```

![AMD Konvertierung Beispiel 1 Strukturlayout](../build/media/vcamd_conv_ex_1_block.png "Strukturlayout für AMD Konvertierung Beispiel 1")

## <a name="example-2"></a>Beispiel 2

```C
// Total size = 24 bytes, alignment = 8 bytes (quadword).

_declspec(align(8)) struct {
    int a;       // +0; size = 4 bytes
    double b;    // +8; size = 8 bytes
    short c;     // +16; size = 2 bytes
}
```

![AMD Konvertierung Beispiel 2 Strukturlayout](../build/media/vcamd_conv_ex_2_block.png "Strukturlayout für AMD Konvertierung Beispiel 2")

## <a name="example-3"></a>Beispiel 3

```C
// Total size = 22 bytes, alignment = 4 bytes (doubleword).

_declspec(align(4)) struct {
    char a;       // +0; size = 1 byte
    short b;      // +2; size = 2 bytes
    char c;       // +4; size = 1 byte
    int d;        // +8; size = 4 bytes
}
```

![AMD Konvertierung Beispiel 2 Strukturlayout](../build/media/vcamd_conv_ex_3_block.png "Strukturlayout für AMD Konvertierung Beispiel 2")

## <a name="example-4"></a>Beispiel 4

```C
// Total size = 8 bytes, alignment = 8 bytes (quadword).

_declspec(align(8)) union {
    char *p;      // +0; size = 8 bytes
    short s;      // +0; size = 2 bytes
    long l;       // +0; size = 4 bytes
}
```

![AMD Konvertierung Beispiel 4 union Layouit](../build/media/vcamd_conv_ex_4_block.png "AMD Konvertierung Beispiel 4 union Layouit")

## <a name="see-also"></a>Siehe auch

[Typen und Speicher](../build/types-and-storage.md)<br/>
