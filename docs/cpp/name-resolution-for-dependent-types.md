---
title: Namensauflösung für abhängige Typen
ms.date: 11/04/2016
ms.assetid: 34066bb4-0c79-4fd8-bda7-539a60a277ab
ms.openlocfilehash: 04db4b0efc5e58dbd3de6fc9979c3a3cdd44d84e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50563151"
---
# <a name="name-resolution-for-dependent-types"></a>Namensauflösung für abhängige Typen

Verwendung **Typename** für qualifizierte Namen in Vorlagendefinitionen, um dem Compiler mitzuteilen, dass der angegebene qualifizierte Name einen Typ bezeichnet. Weitere Informationen finden Sie unter [Typename](../cpp/typename.md).

```cpp
// template_name_resolution1.cpp
#include <stdio.h>
template <class T> class X
{
public:
   void f(typename T::myType* mt) {}
};

class Yarg
{
public:
   struct myType { };
};

int main()
{
   X<Yarg> x;
   x.f(new Yarg::myType());
   printf("Name resolved by using typename keyword.");
}
```

```Output
Name resolved by using typename keyword.
```

Namenssuche nach abhängigen Namen überprüft sowohl der Kontext der Vorlagendefinition Namen – im folgenden Beispiel würde dieser Kontext finden `myFunction(char)`– und den Kontext der Vorlageninstanziierung. Im folgenden Beispiel wird die Vorlage in Main instanziiert werden. aus diesem Grund die `MyNamespace::myFunction` ist ab dem Zeitpunkt der Instanziierung sichtbar und wird als bessere Übereinstimmung ausgewählt. Wenn `MyNamespace::myFunction` umbenannt wurde, wird stattdessen `myFunction(char)` aufgerufen.

Alle Namen werden aufgelöst, als ob sie abhängige Namen wären. Dennoch wird empfohlen, vollqualifizierte Namen zu verwenden, wenn ein möglicher Konflikte besteht.

```cpp
// template_name_resolution2.cpp
// compile with: /EHsc
#include <iostream>
using namespace std;

void myFunction(char)
{
   cout << "Char myFunction" << endl;
}

template <class T> class Class1
{
public:
   Class1(T i)
   {
      // If replaced with myFunction(1), myFunction(char)
      // will be called
      myFunction(i);
}
};

namespace MyNamespace
{
   void myFunction(int)
   {
      cout << "Int MyNamespace::myFunction" << endl;
   }
};

using namespace MyNamespace;

int main()
{
   Class1<int>* c1 = new Class1<int>(100);
}
```

### <a name="output"></a>Output

```Output
Int MyNamespace::myFunction
```

### <a name="template-disambiguation"></a>Vorlagenmehrdeutigkeit

Visual Studio 2012 setzt die C ++ 98/03/11-Standardregeln für Mehrdeutigkeit mit dem Schlüsselwort "Template". Im folgenden Beispiel würde Visual C++ 2010 sowohl die nicht konformen Zeilen als auch die konformen Zeilen akzeptieren.  Visual Studio 2012 akzeptiert nur die konformen Zeilen.

```cpp
#include <iostream>
#include <ostream>
#include <typeinfo>
using namespace std;

template <typename T> struct Allocator {
    template <typename U> struct Rebind {
        typedef Allocator<U> Other;
    };
};

template <typename X, typename AY> struct Container {
    #if defined(NONCONFORMANT)
        typedef typename AY::Rebind<X>::Other AX; // nonconformant
    #elif defined(CONFORMANT)
        typedef typename AY::template Rebind<X>::Other AX; // conformant
    #else
        #error Define NONCONFORMANT or CONFORMANT.
    #endif
};

int main() {
    cout << typeid(Container<int, Allocator<float>>::AX).name() << endl;
}
```

Eine Übereinstimmung mit den Mehrdeutigkeitsregeln ist erforderlich, da C++ standardmäßig annimmt, dass `AY::Rebind` keine Vorlage ist, und der Compiler deshalb folgenden "`<`"-Code als "less-than" interpretiert. Er muss wissen, dass `Rebind` eine Vorlage darstellt, sodass er "`<`" ordnungsgemäß als spitze Klammer analysieren kann.

## <a name="see-also"></a>Siehe auch

[Namensauflösung](../cpp/templates-and-name-resolution.md)