---
title: CD2DSizeU-Klasse
ms.date: 11/04/2016
f1_keywords:
- CD2DSizeU
- AFXRENDERTARGET/CD2DSizeU
- AFXRENDERTARGET/CD2DSizeU::CD2DSizeU
- AFXRENDERTARGET/CD2DSizeU::IsNull
helpviewer_keywords:
- CD2DSizeU [MFC], CD2DSizeU
- CD2DSizeU [MFC], IsNull
ms.assetid: 6e679ba8-2112-43c3-8275-70b660856f02
ms.openlocfilehash: bad73a53eabe0a4c75483e9871a4fdc4a361449b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50512475"
---
# <a name="cd2dsizeu-class"></a>CD2DSizeU-Klasse

Ein Wrapper für D2D1_SIZE_U.

## <a name="syntax"></a>Syntax

```
class CD2DSizeU : public D2D1_SIZE_U;
```

## <a name="members"></a>Member

### <a name="public-constructors"></a>Öffentliche Konstruktoren

|Name|Beschreibung|
|----------|-----------------|
|[CD2DSizeU::CD2DSizeU](#cd2dsizeu)|Überladen. Erstellt eine `CD2DSizeU` -Sitzungsobjekts `D2D1_SIZE_U` Objekt.|

### <a name="public-methods"></a>Öffentliche Methoden

|Name|Beschreibung|
|----------|-----------------|
|[CD2DSizeU::IsNull](#isnull)|Gibt eine **booleschen** Wert, der angibt, ob ein Ausdruck keine gültigen Daten (NULL) enthält.|

### <a name="public-operators"></a>Öffentliche Operatoren

|Name|Beschreibung|
|----------|-----------------|
|[CD2DSizeU::Operator CSize](#operator_csize)|Konvertiert `CD2DSizeU` zu `CSize` Objekt.|

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

`D2D1_SIZE_U`

[CD2DSizeU](../../mfc/reference/cd2dsizeu-class.md)

## <a name="requirements"></a>Anforderungen

**Header:** afxrendertarget.h

##  <a name="cd2dsizeu"></a>  CD2DSizeU::CD2DSizeU

Erstellt ein Objekt CD2DSizeU aus CSize-Objekt.

```
CD2DSizeU(const CSize& size);
CD2DSizeU(const D2D1_SIZE_U& size);
  CD2DSizeU(const D2D1_SIZE_U* size);

CD2DSizeU(
    UINT32 cx = 0,
    UINT32 cy = 0);
```

### <a name="parameters"></a>Parameter

*size*<br/>
Größe der Datenquelle

*CX*<br/>
Source-Breite

*CY*<br/>
Quelle Höhe

##  <a name="isnull"></a>  CD2DSizeU::IsNull

Gibt einen booleschen Wert, der angibt, ob ein Ausdruck keine gültigen Daten (Null) enthält.

```
BOOL IsNull() const;
```

### <a name="return-value"></a>Rückgabewert

True, wenn die Breite und Höhe leer sind. andernfalls "false".

##  <a name="operator_csize"></a>  CD2DSizeU::Operator CSize

CD2DSizeU konvertiert in CSize-Objekt.

```
operator CSize();
```

### <a name="return-value"></a>Rückgabewert

Aktuelle Wert der D2D-Größe.

## <a name="see-also"></a>Siehe auch

[Klassen](../../mfc/reference/mfc-classes.md)
