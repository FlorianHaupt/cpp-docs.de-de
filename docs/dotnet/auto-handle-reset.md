---
title: auto_handle::reset
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- auto_handle.reset
- msclr::auto_handle::reset
- auto_handle::reset
- msclr.auto_handle.reset
helpviewer_keywords:
- auto_handle::reset
ms.assetid: 32dc3a83-80fd-45c9-8f79-8c4096c30f57
ms.openlocfilehash: cd4d29400b34658e9afb64d47ff3a54ec0ee61eb
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50459838"
---
# <a name="autohandlereset"></a>auto_handle::reset

Zerstören Sie das aktuelle Objekt für die im Besitz des Benutzers und optional ein neues Objekt besitzt.

## <a name="syntax"></a>Syntax

```
void reset(
   _element_type ^ _new_ptr
);
void reset();
```

#### <a name="parameters"></a>Parameter

*_new_ptr*<br/>
(Optional) Das neue Objekt.

## <a name="example"></a>Beispiel

```
// msl_auto_handle_reset.cpp
// compile with: /clr
#include <msclr\auto_handle.h>

using namespace System;
using namespace msclr;

ref class ClassA {
   String^ m_s;
public:
   ClassA( String^ s ) : m_s( s ) {
      Console::WriteLine( "ClassA constructor: " + m_s );
   }
   ~ClassA() {
      Console::WriteLine( "ClassA destructor: " + m_s );
   }

   void PrintHello() {
      Console::WriteLine( "Hello from {0} A!", m_s );
   }
};

int main()
{
   auto_handle<ClassA> agc1 = gcnew ClassA( "first" );
   agc1->PrintHello();

   ClassA^ ha = gcnew ClassA( "second" );
   agc1.reset( ha ); // release first object, reference second
   agc1->PrintHello();

   agc1.reset(); // release second object, set to nullptr

   Console::WriteLine( "done" );
}
```

```Output
ClassA constructor: first
Hello from first A!
ClassA constructor: second
ClassA destructor: first
Hello from second A!
ClassA destructor: second
done
```

## <a name="requirements"></a>Anforderungen

**Headerdatei** \<msclr\auto_handle.h >

**Namespace** Msclr

## <a name="see-also"></a>Siehe auch

[auto_handle-Members](../dotnet/auto-handle-members.md)<br/>
[auto_handle::release](../dotnet/auto-handle-release.md)