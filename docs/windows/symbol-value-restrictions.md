---
title: Beschränkungen bei Symbolwerten
ms.date: 11/04/2016
f1_keywords:
- vc.editors.symbol.restrictions.value
helpviewer_keywords:
- symbols [C++], value restrictions
- restrictions, symbol values
ms.assetid: 32467ec3-690b-4cd0-a4d0-7d189a3296cb
ms.openlocfilehash: 0f0a02c7eb2bbb205f41aaeec209c45d629f0b20
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50677668"
---
# <a name="symbol-value-restrictions"></a>Beschränkungen bei Symbolwerten

Bei einem Symbolwert kann es sich um eine beliebige Ganzzahl handeln, die in normaler Form für „#define preprocessor“-Anweisungen ausgedrückt wird. Hier sind einige Beispiele für Symbolwerte:

```
18
4001
0x0012
-3456
```

Bei Symbolwerten für Ressourcen (Zugriffstaste, Bitmaps, Cursor, Dialogfelder, Symbole, Menüs, Zeichenfolgentabellen und Versionsinformationen) muss es sich um Dezimalzahlen im Bereich von 0 bis 32.767 handeln (darf nicht hexadezimal sein). Symbolwerte für Ressourcenbestandteile wie Dialogfeldsteuerelemente oder einzelne Zeichenfolgen in der Zeichenfolgentabelle können von 0 bis 65.534 oder von -32.768 bis 32.767 reichen.

Bei Ressourcensymbolen handelt es sich um 16-Bit-Zahlen. Sie können sie signiert oder nicht signiert eingeben. Sie werden jedoch intern als nicht signierte Ganzzahlen verwendet. Negative Zahlen werden demnach in ihre entsprechenden positiven Werte umgewandelt.

Im Folgenden finden Sie einige Beschränkungen für Symbolwerte:

- Die Visual Studio-Entwicklungsumgebung und MFC verwenden einige Zahlenbereiche für besondere Zwecke. Alle Zahlen mit dem wichtigsten Bitset (-32.768 bis -1 oder 32.768 bis 65.534 in Abhängigkeit des Zeichens) sind für MFC reserviert.

- Es ist nicht möglich, einen Symbolwert mithilfe von anderen Symbolzeichenfolgen zu definieren. Beispielsweise wird die folgende Symboldefinition nicht unterstützt:

    ```cpp
    #define IDC_MYEDIT  IDC_OTHEREDIT  //not supported
    ```

- Sie können Präprozessormakros mit Argumenten nicht als Wertdefinitionen verwenden. Zum Beispiel:

    ```cpp
    #define   IDD_ABOUT  ID(7) //not supported
    ```

   Ist kein gültiger Ausdruck, unabhängig davon, was `ID` zum Zeitpunkt der Kompilierung auswertet.

- Ihre Anwendung verfügt möglicherweise über eine vorhandene Datei, die mit Ausdrücken definierte Symbole enthält. Weitere Informationen zum Einschließen der Symbole als schreibgeschützte Symbole finden Sie unter [gemeinsam genutzter (schreibgeschützter) oder berechneter Symbole](../windows/including-shared-read-only-or-calculated-symbols.md).

Weitere Informationen über Zahlenbereiche finden Sie unter [TN023: MFC-Standardressourcen](../mfc/tn023-standard-mfc-resources.md).

## <a name="requirements"></a>Anforderungen

Win32

## <a name="see-also"></a>Siehe auch

[Ändern des numerischen Werts eines Symbols](../windows/changing-a-symbol-s-numeric-value.md)<br/>
[Beschränkungen bei Symbolnamen](../windows/symbol-name-restrictions.md)<br/>
[Vordefinierte Symbol-IDs](../windows/predefined-symbol-ids.md)