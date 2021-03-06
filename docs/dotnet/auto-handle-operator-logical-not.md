---
title: auto_handle::operator!
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- msclr.auto_handle.operator!
- msclr::auto_handle::operator!
- auto_handle.operator!
- auto_handle::operator!
helpviewer_keywords:
- operator!
ms.assetid: 3f6c7729-3260-4842-87f9-c491c140b299
ms.openlocfilehash: 37c5a35d2cecd3e2e6bc58994fc54704f9169200
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50558170"
---
# <a name="autohandleoperator"></a>auto_handle::operator!

Operator für die Verwendung von `auto_handle` in einem bedingten Ausdruck.

## <a name="syntax"></a>Syntax

```
bool operator!();
```

## <a name="return-value"></a>Rückgabewert

**"true"** ist das umschlossene Objekt ungültig; **"false"** andernfalls.

## <a name="example"></a>Beispiel

```cpp
// msl_auto_handle_operator_not.cpp
// compile with: /clr
#include <msclr\auto_handle.h>

using namespace System;
using namespace msclr;

int main() {
   auto_handle<String> s1;
   auto_handle<String> s2 = "something";
   if ( s1) Console::WriteLine( "s1 is valid" );
   if ( !s1 ) Console::WriteLine( "s1 is invalid" );
   if ( s2 ) Console::WriteLine( "s2 is valid" );
   if ( !s2 ) Console::WriteLine( "s2 is invalid" );
   s2.reset();
   if ( s2 ) Console::WriteLine( "s2 is now valid" );
   if ( !s2 ) Console::WriteLine( "s2 is now invalid" );
}
```

```Output
s1 is invalid
s2 is valid
s2 is now invalid
```

## <a name="requirements"></a>Anforderungen

**Headerdatei** \<msclr\auto_handle.h >

**Namespace** Msclr

## <a name="see-also"></a>Siehe auch

[auto_handle-Members](../dotnet/auto-handle-members.md)<br/>
[auto_handle::operator bool](../dotnet/auto-handle-operator-bool.md)