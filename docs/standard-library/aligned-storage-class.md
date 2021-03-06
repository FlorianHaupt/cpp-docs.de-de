---
title: aligned_storage-Klasse
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::aligned_storage
helpviewer_keywords:
- aligned_storage class
- aligned_storage
ms.assetid: f255e345-1f05-4d07-81e4-017f420839fb
ms.openlocfilehash: 6a3145cb1837a3ea95c48022db391ddbccf55199
ms.sourcegitcommit: afd6fac7c519dbc47a4befaece14a919d4e0a8a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2018
ms.locfileid: "51517162"
---
# <a name="alignedstorage-class"></a>aligned_storage-Klasse

Erstellt einen entsprechend ausgerichteten Typ.

## <a name="syntax"></a>Syntax

```cpp
template <std::size_t Len, std::size_t Align>
struct aligned_storage;

template <std::size_t Len, std::size_t Align = alignment_of<max_align_t>::value>
using aligned_storage_t = typename aligned_storage<Len, Align>::type;
```

### <a name="parameters"></a>Parameter

*Len*<br/>
Die Objektgröße.

*Ausrichten*<br/>
Die Objektausrichtung.

## <a name="remarks"></a>Hinweise

Der TypeDef-Member von Vorlage `type` ist ein Synonym für einen POD-Typ, mit der Ausrichtung *ausrichten* und Größe *Len*. *Ausrichten* muss gleich sein `alignment_of<T>::value` für einen Typ `T`, oder klicken Sie mit der standardmäßigen Ausrichtung.

## <a name="example"></a>Beispiel

```cpp
#include <type_traits>
#include <iostream>

typedef std::aligned_storage<sizeof (int),
    std::alignment_of<double>::value>::type New_type;
int main()
    {
    std::cout << "alignment_of<int> == "
        << std::alignment_of<int>::value << std::endl;
    std::cout << "aligned to double == "
        << std::alignment_of<New_type>::value << std::endl;

    return (0);
    }
```

```Output
alignment_of<int> == 4
aligned to double == 8
```

## <a name="requirements"></a>Anforderungen

**Header:** \<type_traits>

**Namespace:** std

## <a name="see-also"></a>Siehe auch

[<type_traits>](../standard-library/type-traits.md)<br/>
[alignment_of-Klasse](../standard-library/alignment-of-class.md)<br/>
