---
title: SRWLockExclusiveTraits-Struktur
ms.date: 09/27/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::GetInvalidValue
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::Unlock
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::GetInvalidValue method
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::Unlock method
ms.assetid: 38a996ef-c2d7-4886-b413-a426ecee8f05
ms.openlocfilehash: 4005f0dc1f75b79650963efc9a6f9f7522bc3395
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50476465"
---
# <a name="srwlockexclusivetraits-structure"></a>SRWLockExclusiveTraits-Struktur

Beschreibt die allgemeinen Merkmale der `SRWLock` Klasse im Sperrmodus für exklusive.

## <a name="syntax"></a>Syntax

```cpp
struct SRWLockExclusiveTraits;
```

## <a name="members"></a>Member

### <a name="public-typedefs"></a>Öffentliche Typedefs

Name   | Beschreibung
------ | --------------------------------------------------------------------------
`Type` | Synonym für einen Zeiger auf die [SRWLOCK](../windows/srwlock-class.md) Klasse.

### <a name="public-methods"></a>Öffentliche Methoden

Name                                                        | Beschreibung
----------------------------------------------------------- | --------------------------------------------------------------------
[Srwlockexclusivetraits:: Getinvalidvalue](#getinvalidvalue) | Ruft eine `SRWLockExclusiveTraits` -Objekt, das immer ungültig ist.
[Srwlockexclusivetraits:: Unlock](#unlock)                   | Exklusive Kontrolle über den angegebenen Versionen `SRWLock` Objekt.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

`SRWLockExclusiveTraits`

## <a name="requirements"></a>Anforderungen

**Header:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::HandleTraits

## <a name="getinvalidvalue"></a>Srwlockexclusivetraits:: Getinvalidvalue

Ruft eine `SRWLockExclusiveTraits` -Objekt, das immer ungültig ist.

```cpp
inline static Type GetInvalidValue();
```

### <a name="return-value"></a>Rückgabewert

Ein leeres `SRWLockExclusiveTraits`-Objekt.

## <a name="unlock"></a>Srwlockexclusivetraits:: Unlock

Exklusive Kontrolle über den angegebenen Versionen `SRWLock` Objekt.

```cpp
inline static void Unlock(
   _In_ Type srwlock
);
```

### <a name="parameters"></a>Parameter

*SRWLOCK*<br/>
Handle für ein `SRWLock` Objekt.
