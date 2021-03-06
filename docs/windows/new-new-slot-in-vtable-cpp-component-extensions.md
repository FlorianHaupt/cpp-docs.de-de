---
title: New (neuer Slot in Vtable) (C++ / CLI und C++ / CX)
ms.date: 10/12/2018
ms.topic: reference
helpviewer_keywords:
- new keyword [C++]
ms.assetid: 1a9a5704-f02f-46ae-ad65-f0f2b6dbabc3
ms.openlocfilehash: b143b2ead1165382d0959f4e4c90f1d2e7ea936a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50487164"
---
# <a name="new-new-slot-in-vtable--ccli-and-ccx"></a>New (neuer Slot in Vtable) (C++ / CLI und C++ / CX)

Die **neue** -Schlüsselwort Gibt an, dass ein virtueller Member einen neuen Platz im Vtable erhält.

## <a name="all-runtimes"></a>Alle Laufzeiten

(Es gibt keine Hinweise für diese Sprachfunktion, die für alle Laufzeiten gültig sind.)

## <a name="windows-runtime"></a>Windows-Runtime

In Windows-Runtime unterstützt nicht.

## <a name="common-language-runtime"></a>Common Language Runtime

### <a name="remarks"></a>Hinweise

In einem `/clr` Kompilierung **neue** gibt an, dass ein virtueller Member einen neuen Platz im Vtable erhält; dass die Funktion eine Methode der Basisklasse nicht überschreibt.

**neue** bewirkt, dass den Newslot-Modifizierer dem IL für die Funktion hinzugefügt werden.  Weitere Informationen zu "newslot" finden Sie unter:

- [MethodInfo.GetBaseDefinition-Methode](https://msdn.microsoft.com/library/system.reflection.methodinfo.getbasedefinition.aspx)

- [MethodAttributes-Enumeration](https://msdn.microsoft.com/library/system.reflection.methodattributes.aspx)

### <a name="requirements"></a>Anforderungen

Compileroption: `/clr`

### <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Auswirkungen der **neue**.

```cpp
// newslot.cpp
// compile with: /clr
ref class C {
public:
   virtual void f() {
      System::Console::WriteLine("C::f() called");
   }

   virtual void g() {
      System::Console::WriteLine("C::g() called");
   }
};

ref class D : public C {
public:
   virtual void f() new {
      System::Console::WriteLine("D::f() called");
   }

   virtual void g() override {
      System::Console::WriteLine("D::g() called");
   }
};

ref class E : public D {
public:
   virtual void f() override {
      System::Console::WriteLine("E::f() called");
   }
};

int main() {
   D^ d = gcnew D;
   C^ c = gcnew D;

   c->f();   // calls C::f
   d->f();   // calls D::f

   c->g();   // calls D::g
   d->g();   // calls D::g

   D ^ e = gcnew E;
   e->f();   // calls E::f
}
```

```Output
C::f() called

D::f() called

D::g() called

D::g() called

E::f() called
```

## <a name="see-also"></a>Siehe auch

[Komponentenerweiterungen für .NET und UWP](../windows/component-extensions-for-runtime-platforms.md)<br/>

[Überschreibungsspezifizierer](../windows/override-specifiers-cpp-component-extensions.md)