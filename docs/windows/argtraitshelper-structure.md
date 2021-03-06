---
title: ArgTraitsHelper-Struktur
ms.date: 09/21/2018
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::Details::ArgTraitsHelper
- event/Microsoft::WRL::Details::ArgTraitsHelper::args
helpviewer_keywords:
- Microsoft::WRL::Details::ArgTraitsHelper structure
- Microsoft::WRL::Details::ArgTraitsHelper::args constant
ms.assetid: e3f798da-0aef-4a57-95d3-d38c34c47d72
ms.openlocfilehash: fbba6d96106cc95910ccd9d0029cb3e9c254d7d3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50629904"
---
# <a name="argtraitshelper-structure"></a>ArgTraitsHelper-Struktur

Unterstützt die Infrastruktur von WRL und nicht direkt aus Ihrem Code verwendet werden soll.

## <a name="syntax"></a>Syntax

```cpp
template<typename TDelegateInterface>
struct ArgTraitsHelper;
```

### <a name="parameters"></a>Parameter

*TDelegateInterface*<br/>
Ein Delegat-Schnittstelle.

## <a name="remarks"></a>Hinweise

Hilft, die gemeinsamen Merkmale der Argumente des Delegaten definieren.

## <a name="members"></a>Member

### <a name="public-typedefs"></a>Öffentliche Typedefs

Name         | Beschreibung
------------ | ------------------------------------------------------
`methodType` | Ein Synonym für `decltype(&TDelegateInterface::Invoke)`.
`Traits`     | Ein Synonym für `ArgTraits<methodType>`.

### <a name="public-constants"></a>Öffentliche Konstanten

name                           | Beschreibung
------------------------------ | ---------------------------------------------------------------------------------------------------------------------
[Argtraitshelper:: args](#args) | Hilft [argtraits:: args](#args) behalten Sie die Anzahl der Parameter der `Invoke` Methode einer Schnittstelle des Delegaten.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

`ArgTraitsHelper`

## <a name="requirements"></a>Anforderungen

**Header:** event.h

**Namespace:** Microsoft::WRL::Details

## <a name="args"></a>Argtraitshelper:: args

Unterstützt die Infrastruktur von WRL und nicht direkt aus Ihrem Code verwendet werden soll.

```cpp
static const int args = Traits::args;
```

### <a name="remarks"></a>Hinweise

Hilft `ArgTraitsHelper::args` behalten Sie die Anzahl der Parameter der `Invoke` Methode einer Schnittstelle des Delegaten.
