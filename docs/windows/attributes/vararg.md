---
title: Vararg (C++-COM-Attribut)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.vararg
helpviewer_keywords:
- vararg attribute
ms.assetid: 20fc3244-18e9-411c-990e-d5b4fa29a570
ms.openlocfilehash: 6f3048e60c10efed05fc5bccc3c61949351f7bf9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50504701"
---
# <a name="vararg"></a>vararg

Gibt an, dass die Funktion eine Variable Anzahl von Argumenten akzeptiert.

## <a name="syntax"></a>Syntax

```cpp
[vararg]
```

## <a name="remarks"></a>Hinweise

Die **Vararg** C++-Attribut hat die gleiche Funktionalität wie die [Vararg](/windows/desktop/Midl/vararg) MIDL-Attribut.

## <a name="example"></a>Beispiel

Der folgende Code veranschaulicht die Verwendung der **Vararg**:

```cpp
// cpp_attr_ref_vararg.cpp
// compile with: /LD
#include "unknwn.h"
#include "oaidl.h"
[module(name="MyLibrary")];

[object, uuid("00000000-0000-0000-0000-000000000001")]
__interface X : public IUnknown
{
   [vararg] HRESULT Button([in, satype(VARIANT)]SAFEARRAY *psa);
};
```

## <a name="requirements"></a>Anforderungen

### <a name="attribute-context"></a>Attributkontext

|||
|-|-|
|**Betrifft**|Schnittstellenmethode|
|**Wiederholbar**|Nein|
|**Erforderliche Attribute**|Keiner|
|**Ungültige Attribute**|Keiner|

Weitere Informationen zu den Attributkontexten finden Sie unter [Attributkontexte](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>Siehe auch

[IDL-Attribute](idl-attributes.md)<br/>
[Methodenattribut](method-attributes.md)