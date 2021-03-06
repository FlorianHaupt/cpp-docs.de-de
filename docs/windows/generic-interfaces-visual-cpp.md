---
title: Generische Schnittstellen (C++ / CLI)
ms.date: 10/12/2018
ms.topic: reference
helpviewer_keywords:
- generic interfaces
- interfaces, generic [C++}
ms.assetid: f3da788a-ba83-4db7-9dcf-9b95a8fb9d1a
ms.openlocfilehash: 68c5a53d3de38479adbdcb49e823513f295a2095
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50493950"
---
# <a name="generic-interfaces-ccli"></a>Generische Schnittstellen (C++ / CLI)

Die Einschränkungen für Typparameter für Klassen sind identisch mit denen, die Typparameter für Schnittstellen gelten (finden Sie unter [generische Klassen (C++ / CLI)](../windows/generic-classes-cpp-cli.md)).

Die Regeln, die beim Überladen von Funktionen steuern, sind für Funktionen innerhalb von generischen Klassen oder generischen Schnittstellen gleich.

Explizite schnittstellenimplementierungen für Member arbeiten mit konstruierte Schnittstellentypen in die gleiche Weise wie bei einfachen Schnittstellentypen (siehe die folgenden Beispielen).

Weitere Informationen zu den Schnittstellen, finden Sie unter [Schnittstellenklasse](../windows/interface-class-cpp-component-extensions.md).

## <a name="syntax"></a>Syntax

```cpp
[attributes] generic <class-key type-parameter-identifier[, ...]>
[type-parameter-constraints-clauses][accesibility-modifiers] interface class identifier [: base-list] {   interface-body} [declarators] ;
```

## <a name="remarks"></a>Hinweise

*Attribute*<br/>
(Optional) Zusätzliche deklarative Informationen. Weitere Informationen zu Attributen und Attributklassen finden Sie unter **Attribute**.

*Klassenschlüssel*<br/>
**Klasse** oder **Typename**

*type-parameter-identifier(s)*<br/>
Liste der durch Trennzeichen getrennte IDs.

*Type-Parameter-Einschränkungen-Klauseln*<br/>
Nimmt die Form, die im angegebenen [Einschränkungen für generische Typparameter (C++ / CLI)](../windows/constraints-on-generic-type-parameters-cpp-cli.md)

*Zugriffsmodifizierer*<br/>
(Optional) Zugriffsmodifizierer (z. B. **öffentliche, private**).

*identifier*<br/>
Der Name der Schnittstelle.

*Base-list*<br/>
(Optional) Eine Liste, die eine oder mehrere explizite Basisschnittstelle durch Kommas getrennt enthält.

*Interface-body*<br/>
Deklarationen der Schnittstellenmember.

*Deklaratoren*<br/>
(Optional) Deklarationen von Variablen, die auf diesem Typ basiert.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie zum Deklarieren und Instanziieren einer generischen Schnittstelle wird. Im Beispiel ist die generische Schnittstelle `IList<ItemType>` deklariert wird. Es wird dann implementiert, indem zwei generischen Klassen `List1<ItemType>` und `List2<ItemType>`, mit verschiedenen Implementierungen.

```cpp
// generic_interface.cpp
// compile with: /clr
using namespace System;

// An exception to be thrown by the List when
// attempting to access elements beyond the
// end of the list.
ref class ElementNotFoundException : Exception {};

// A generic List interface
generic <typename ItemType>
public interface class IList {
   ItemType MoveFirst();
   bool Add(ItemType item);
   bool AtEnd();
   ItemType Current();
   void MoveNext();
};

// A linked list implementation of IList
generic <typename ItemType>
public ref class List1 : public IList<ItemType> {
   ref class Node {
      ItemType m_item;

   public:
      ItemType get_Item() { return m_item; };
      void set_Item(ItemType value) { m_item = value; };

      Node^ next;

      Node(ItemType item) {
         m_item = item;
         next = nullptr;
      }
   };

   Node^ first;
   Node^ last;
   Node^ current;

   public:
   List1() {
      first = nullptr;
      last = first;
      current = first;
   }

   virtual ItemType MoveFirst() {
      current = first;
      if (first != nullptr)
        return first->get_Item();
      else
         return ItemType();
   }

   virtual bool Add(ItemType item) {
      if (last != nullptr) {
         last->next = gcnew Node(item);
         last = last->next;
      }
      else {
         first = gcnew Node(item);
         last = first;
         current = first;
      }
      return true;
   }

   virtual bool AtEnd() {
      if (current == nullptr )
        return true;
      else
        return false;
   }

   virtual ItemType Current() {
       if (current != nullptr)
         return current->get_Item();
       else
         throw gcnew ElementNotFoundException();
   }

   virtual void MoveNext() {
      if (current != nullptr)
       current = current->next;
      else
        throw gcnew ElementNotFoundException();
   }
};

// An array implementation of IList
generic <typename ItemType>
ref class List2 : public IList<ItemType> {
   array<ItemType>^ item_array;
   int count;
   int current;

   public:

   List2() {
      // not yet possible to declare an
      // array of a generic type parameter
      item_array = gcnew array<ItemType>(256);
      count = current = 0;
   }

   virtual ItemType MoveFirst() {
      current = 0;
      return item_array[0];
   }

   virtual bool Add(ItemType item) {
      if (count < 256)
         item_array[count++] = item;
      else
        return false;
      return true;
   }

   virtual bool AtEnd() {
      if (current >= count)
        return true;
      else
        return false;
   }

   virtual ItemType Current() {
      if (current < count)
        return item_array[current];
      else
        throw gcnew ElementNotFoundException();
   }

   virtual void MoveNext() {
      if (current < count)
         ++current;
      else
         throw gcnew ElementNotFoundException();
   }
};

// Add elements to the list and display them.
generic <typename ItemType>
void AddStringsAndDisplay(IList<ItemType>^ list, ItemType item1, ItemType item2) {
   list->Add(item1);
   list->Add(item2);
   for (list->MoveFirst(); ! list->AtEnd(); list->MoveNext())
   Console::WriteLine(list->Current());
}

int main() {
   // Instantiate both types of list.

   List1<String^>^ list1 = gcnew List1<String^>();
   List2<String^>^ list2 = gcnew List2<String^>();

   // Use the linked list implementation of IList.
   AddStringsAndDisplay<String^>(list1, "Linked List", "List1");

   // Use the array implementation of the IList.
   AddStringsAndDisplay<String^>(list2, "Array List", "List2");
}
```

```Output
Linked List
List1
Array List
List2
```

## <a name="example"></a>Beispiel

Das folgende Beispiel deklariert eine generische Schnittstelle `IMyGenIface`, und zwei nicht generischen Schnittstellen `IMySpecializedInt` und `ImySpecializedString`, spezialisiert, die `IMyGenIface`. Die beiden spezialisierten Schnittstellen werden dann durch zwei Klassen, implementiert `MyIntClass` und `MyStringClass`. Das Beispiel zeigt, wie generische Schnittstellen spezialisiert, Instanziieren von generischen und nicht generischen Schnittstellen und rufen Sie die explizit implementierten Member für die Schnittstellen.

```cpp
// generic_interface2.cpp
// compile with: /clr
// Specializing and implementing generic interfaces.
using namespace System;

generic <class ItemType>
public interface class IMyGenIface {
   void Initialize(ItemType f);
};

public interface class IMySpecializedInt: public IMyGenIface<int> {
   void Display();
};

public interface class IMySpecializedString: public IMyGenIface<String^> {
   void Display();
};

public ref class MyIntClass: public IMySpecializedInt {
   int myField;

public:
   virtual void Initialize(int f) {
      myField = f;
   }

   virtual void Display() {
      Console::WriteLine("The integer field contains: {0}", myField);
   }
};

public ref struct MyStringClass: IMySpecializedString {
   String^ myField;

public:
   virtual void Initialize(String^ f) {
      myField = f;
    }

   virtual void Display() {
      Console::WriteLine("The String field contains: {0}", myField);
   }
};

int main() {
   // Instantiate the generic interface.
   IMyGenIface<int>^ myIntObj = gcnew MyIntClass();

   // Instantiate the specialized interface "IMySpecializedInt."
   IMySpecializedInt^ mySpIntObj = (IMySpecializedInt^) myIntObj;

   // Instantiate the generic interface.
   IMyGenIface<String^>^ myStringObj = gcnew MyStringClass();

   // Instantiate the specialized interface "IMySpecializedString."
   IMySpecializedString^ mySpStringObj =
            (IMySpecializedString^) myStringObj;

   // Call the explicitly implemented interface members.
   myIntObj->Initialize(1234);
   mySpIntObj->Display();

   myStringObj->Initialize("My string");
   mySpStringObj->Display();
}
```

```Output
The integer field contains: 1234
The String field contains: My string
```

## <a name="see-also"></a>Siehe auch

[Generika](../windows/generics-cpp-component-extensions.md)