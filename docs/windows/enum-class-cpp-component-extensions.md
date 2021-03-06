---
title: Enum-Klasse (C++ / CLI und C++ / CX)
ms.date: 10/12/2018
ms.topic: reference
ms.assetid: 8010fa8c-bad6-45b4-8214-b4db64d7ffe1
ms.openlocfilehash: 5bc850831e961a500ae71ce90e3ca39b3aabd159
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50592516"
---
# <a name="enum-class--ccli-and-ccx"></a>Enum-Klasse (C++ / CLI und C++ / CX)

Deklariert eine Enumeration im Namespacebereich, die ein benutzerdefinierter Typ ist, der aus einem Satz von benannten Konstanten besteht, die als Enumeratoren bezeichnet werden.

## <a name="all-runtimes"></a>Alle Laufzeiten

### <a name="remarks"></a>Hinweise

C++ / CX und C++ / CLI-Unterstützung **öffentliche Enumerationsklasse** und **private Enumerationsklasse** ähneln sich der c++- **Enumerationsklasse** aber zusätzlich den Zugriff auf Spezifizierer. Unter **"/ CLR"**, C ++ 11 **Enumerationsklasse** -Typ zulässig, jedoch generiert die Warnung C4472, was beabsichtigt ist, um sicherzustellen, dass Sie tatsächlich den ISO-Enumerationstyp und nicht die C++ / CX und C++ / CLI-Typ. Weitere Informationen zu der ISO C++ **Enum** -Schlüsselwort, finden Sie unter [Enumerationen](../cpp/enumerations-cpp.md).

## <a name="windows-runtime"></a>Windows-Runtime

### <a name="syntax"></a>Syntax

```cpp
      access
      enum class
      enumeration-identifier
      [:underlying-type] { enumerator-list } [var];
accessenum structenumeration-identifier[:underlying-type] { enumerator-list } [var];
```

### <a name="parameters"></a>Parameter

*Zugriff*<br/>
Der Zugriff der Enumeration, die möglicherweise **öffentliche** oder **private**.

*enumeration-identifier*<br/>
Der Name der Enumeration.

*underlying-type*<br/>
(Optional) Der zugrunde liegende Typ der Enumeration.

(Optional. Nur Windows-Runtime) der zugrunde liegende Typ der Enumeration, die möglicherweise **"bool"**, **Char**, `char16`, `int16`, `uint16`, **Int**, `uint32`, `int64`, oder `uint64`.

*enumerator-list*<br/>
Eine durch Komma getrennte Liste mit Enumeratornamen.

Der Wert jedes Enumerators ist ein konstanter Ausdruck, der entweder implizit vom Compiler oder explizit durch die Notation *enumerator*`=`*constant-expression*. Standardmäßig ist der Wert des ersten Enumerators Null, wenn er implizit definiert ist. Der Wert jedes folgenden implizit definierten Enumerators ist der Wert des vorherigen Enumerators + 1.

*var*<br/>
(Optional) Der Name einer Variablen des Enumerationstyps.

### <a name="remarks"></a>Hinweise

Weitere Informationen und Beispiele finden Sie unter [Enums](https://msdn.microsoft.com/%20library/windows/apps/hh755820.aspx).

Beachten Sie, dass der Compiler Fehlermeldungen ausgibt, wenn der konstante Ausdruck, der den Wert eines Enumerators definiert, nicht durch den *underlying-type*dargestellt werden kann.  Der Compiler meldet jedoch keinen Fehler für einen Wert, der für den zugrunde liegenden Typ ungeeignet ist. Zum Beispiel:

- Wenn der *underlying-type* numerisch ist und ein Enumerator den maximalen Wert für diesen Typ angibt, kann der Wert der folgenden implizit definierten Enumeration nicht dargestellt werden.

- Wenn *vom zugrunde liegenden Typ* ist **"bool"**, und mehr als zwei Enumeratoren implizit definiert, die Enumeratoren, die ersten beiden nicht dargestellt werden können.

- Wenn der *underlying-type* `char16`ist und der Enumerationswert von 0xD800 bis 0xDFFF reicht, kann der Wert dargestellt werden. Der Wert ist jedoch logisch falsch, da er die Hälfte ein Unicode-Ersatzzeichenpaars darstellt und nicht isoliert angezeigt werden soll.

### <a name="requirements"></a>Anforderungen

Compileroption: `/ZW`

## <a name="common-language-runtime"></a>Common Language Runtime

### <a name="syntax"></a>Syntax

```cpp
      access
      enum class
      name [:type] { enumerator-list } var;
accessenum structname [:type] { enumerator-list } var;
```

### <a name="parameters"></a>Parameter

*Zugriff*<br/>
Die Zugriff der Enumeration. Kann es sich um **öffentliche** oder **private**.

*enumerator-list*<br/>
Eine durch Komma getrennte Liste der Bezeichner (Enumeratoren) in der Enumeration.

*name*<br/>
Der Name der Enumeration. Anonyme verwaltete Enumerationen sind nicht zulässig.

*Typ*<br/>
(Optional) Der zugrunde liegende Typ der *Bezeichner*. Dies kann einen beliebigen skalaren Typ, z. B. Versionen mit oder ohne Vorzeichen von sein **Int**, **kurze**, oder **lange**.  **"bool"** oder **Char** ist ebenfalls zulässig.

*var*<br/>
(Optional) Der Name einer Variablen des Enumerationstyps.

### <a name="remarks"></a>Hinweise

**enum class** und **enum struct** sind entsprechende Deklarationen.

Es gibt zwei Typen von Enumerationen: C++/CX und Standard.

Eine verwaltete oder C++/CX-Enumeration kann wie folgt definiert sein:

```cpp
public enum class day {sun, mon };
```

und ist semantisch äquivalent zu:

```cpp
ref class day {
public:
   static const int sun = 0;
   static const int mon = 1;
};
```

Eine Standard-Enumeration kann wie folgt definiert sein:

```cpp
enum day2 { sun, mon };
```

und ist semantisch äquivalent zu:

```cpp
static const int sun = 0;
static const int mon = 1;
```

Verwaltete Enumeratornamen (*Bezeichner*) werden nicht in den Bereich injiziert, in dem die Enumeration definiert ist. Alle Verweise auf Enumeratoren müssen vollständig qualifiziert sein (*Name*`::`*Bezeichner*).  Aus diesem Grund können Sie keine anonyme verwaltete Enumeration definieren.

Die Enumeratoren einer Standardenumeration werden stark in den einschließenden Bereich eingefügt.  Das heißt, wenn es ein anderes Symbol mit dem gleichen Namen wie ein Enumerator im einschließenden Bereich gibt, generiert der Compiler einen Fehler.

In Visual Studio 2002 und Visual Studio 2003 wurden Enumeratoren schwach eingefügt (sichtbar im einschließenden Bereich es sei denn, gab es einen anderen Bezeichner mit demselben Namen).

Wenn eine standardmäßige C++-Enumeration definiert ist (ohne **Klasse** oder **Struktur**) kompilieren mit `/clr` wird die Enumeration als verwaltete Enumeration kompiliert werden.  Die Enumeration hat weiterhin die Semantik einer nicht verwalteten Enumeration.  Beachten Sie, dass der Compiler Fügt ein Attribut `Microsoft::VisualC::NativeEnumAttribute` zum Identifizieren der Programmierer die Enumeration eine systemeigene Enumeration.  Andere Compiler erkennen einfach die Standardenumeration als verwaltete Enumeration.

Eine benannte, standardenumeration kompiliert, mit `/clr` werden in der Assembly als verwaltete Enumeration sichtbar und können von einem anderen verwalteten Compiler genutzt werden.   Eine unbenannte Standardenumeration ist jedoch nicht öffentlich aus der Assembly sichtbar.

In Visual Studio 2002 und Visual Studio 2003 eine standardenumeration, die als Typ in einem Funktionsparameter verwendet:

```cpp
// mcppv2_enum.cpp
// compile with: /clr
enum E { a, b };
void f(E) {System::Console::WriteLine("hi");}

int main() {
   E myi = b;
   f(myi);
}
```

die folgende in MSIL für die Funktionssignatur ausgeben:

```cpp
void f(int32);
```

In den aktuellen Versionen des Compilers, wird die Standardenumeration als verwaltete Enumeration mit einem [NativeEnumAttribute] und dem folgenden in MSIL für die Funktionssignatur ausgegeben:

```cpp
void f(E)
```

Weitere Informationen zu systemeigenen Enumerationen finden Sie unter [Deklarationen von C++-Enumerationen](../cpp/enumerations-cpp.md).

Weitere Informationen zu CLR-Enumerationen finden Sie unter:

- [Zugrunde liegender Typ eines Enumerators](../dotnet/how-to-define-and-consume-enums-in-cpp-cli.md)

### <a name="requirements"></a>Anforderungen

Compileroption: `/clr`

### <a name="examples"></a>Beispiele

```cpp
// mcppv2_enum_2.cpp
// compile with: /clr
// managed enum
public enum class m { a, b };

// standard enum
public enum n { c, d };

// unnamed, standard enum
public enum { e, f } o;

int main()
{
   // consume managed enum
   m mym = m::b;
   System::Console::WriteLine("no automatic conversion to int: {0}", mym);
   System::Console::WriteLine("convert to int: {0}", (int)mym);

   // consume standard enum
   n myn = d;
   System::Console::WriteLine(myn);

   // consume standard, unnamed enum
   o = f;
   System::Console::WriteLine(o);
}
```

```Output
no automatic conversion to int: b

convert to int: 1

1

1
```

## <a name="see-also"></a>Siehe auch

[Komponentenerweiterungen für .NET und UWP](../windows/component-extensions-for-runtime-platforms.md)