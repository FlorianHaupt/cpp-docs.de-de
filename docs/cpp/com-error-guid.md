---
title: _com_error::GUID
ms.date: 11/04/2016
f1_keywords:
- _com_error::GUID
helpviewer_keywords:
- GUID method [C++]
ms.assetid: e84c2c23-d02e-48f8-b776-9bd6937296d2
ms.openlocfilehash: 905b67577a65b81be0b4d18c7513652dd8c5f055
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50661629"
---
# <a name="comerrorguid"></a>_com_error::GUID

**Microsoft-spezifisch**

Ruft die `IErrorInfo::GetGUID`-Funktion auf.

## <a name="syntax"></a>Syntax

```
GUID GUID( ) const throw( );
```

## <a name="return-value"></a>Rückgabewert

Gibt das Ergebnis des `IErrorInfo::GetGUID` für die `IErrorInfo` -Objekt erfasst wird, innerhalb der `_com_error` Objekt. Wenn kein `IErrorInfo` -Objekt erfasst wird, gibt `GUID_NULL`.

## <a name="remarks"></a>Hinweise

Jeder Fehler beim Aufrufen der `IErrorInfo::GetGUID` -Methode wird ignoriert.

**Ende Microsoft-spezifisch**

## <a name="see-also"></a>Siehe auch

[_com_error-Klasse](../cpp/com-error-class.md)