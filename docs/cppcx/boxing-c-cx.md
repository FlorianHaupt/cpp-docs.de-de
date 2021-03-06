---
title: Boxing (C++/CX)
ms.date: 12/30/2016
ms.assetid: edfb12fa-2a9b-42f6-bdac-d4d76cb8274e
ms.openlocfilehash: c680ea0262e8e65345cba40280a389453c2985bb
ms.sourcegitcommit: afd6fac7c519dbc47a4befaece14a919d4e0a8a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2018
ms.locfileid: "51519515"
---
# <a name="boxing-ccx"></a>Boxing (C++/CX)

Beim*Boxing* wird eine Werttypvariable wie [Windows::Foundation::DateTime](https://msdn.microsoft.com/library/windows/apps/windows.foundation.datetime.aspx)– oder ein grundlegender Skalartyp wie `int`– innerhalb einer Verweisklasse umgebrochen, wenn die Variable an eine Methode übergeben wird, die [Platform::Object^](../cppcx/platform-object-class.md) als Eingabetyp akzeptiert.

## <a name="passing-a-value-type-to-an-object-parameter"></a>Übergeben eines Werttyps an einen Object^-Parameter

Obwohl Sie für eine Variable nicht explizit Boxing anwenden müssen, um sie an einen Methodenparameter des Typs [Platform::Object^](../cppcx/platform-object-class.md)zu übergeben, müssen Sie eine Umwandlung zum ursprünglichen Typ explizit vornehmen, wenn Sie Werte abrufen, die zuvor geschachtelt wurden.

[!code-cpp[cx_boxing#01](../cppcx/codesnippet/CPP/cx_boxing/class1.cpp#01)]

### <a name="using-platformiboxt-to-support-nullable-value-types"></a>Verwenden von Platform:: ibox\<T > zur Unterstützung von auf NULL festlegbare Werttypen

C# und Visual Basic unterstützen das Konzept von Typen, die NULL-Werte zulassen. In C++ / CX können Sie die `Platform::IBox<T>` Typ um öffentliche Methoden verfügbar zu machen, die Werttypparameter unterstützen. Das folgende Beispiel zeigt C++ / CX-öffentliche Methode, die null zurückgibt, wenn ein C#-Aufrufer für eines der Argumente null übergibt.

[!code-cpp[cx_boxing#02](../cppcx/codesnippet/CPP/cx_boxing/class1.h#02)]

In einem C#-XAML-Client können Sie diese Methode wie folgt verwenden:

```

// C# client code
    BoxingDemo.Class1 obj = new BoxingDemo.Class1();
    int? a = null;
    int? b = 5;
    var result = obj.Multiply(a,b); //result = null
```

## <a name="see-also"></a>Siehe auch

[Typsystem (C++/CX)](../cppcx/type-system-c-cx.md)<br/>
[Typumwandlung (C++-CX)](../cppcx/casting-c-cx.md)<br/>
[Sprachreferenz zu Visual C++](../cppcx/visual-c-language-reference-c-cx.md)<br/>
[Namespaceverweis](../cppcx/namespaces-reference-c-cx.md)