---
title: CDefaultCompareTraits-Klasse
ms.date: 11/04/2016
f1_keywords:
- CDefaultCompareTraits
- ATLCOLL/ATL::CDefaultCompareTraits
- ATLCOLL/ATL::CDefaultCompareTraits::CompareElements
- ATLCOLL/ATL::CDefaultCompareTraits::CompareElementsOrdered
helpviewer_keywords:
- CDefaultCompareTraits class
ms.assetid: a17e2740-e7b4-48f2-aeb7-c80ce84b63f7
ms.openlocfilehash: b7f51ccd266fce1b5d614dfe2c725e20fde6f297
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50575304"
---
# <a name="cdefaultcomparetraits-class"></a>CDefaultCompareTraits-Klasse

Diese Klasse stellt die standardmäßige Element Vergleichsfunktionen.

## <a name="syntax"></a>Syntax

```
template<typename T>
class CDefaultCompareTraits
```

#### <a name="parameters"></a>Parameter

*T*<br/>
Der Typ der Daten in der Auflistung gespeichert werden.

## <a name="members"></a>Member

### <a name="public-methods"></a>Öffentliche Methoden

|Name|Beschreibung|
|----------|-----------------|
|[CDefaultCompareTraits::CompareElements](#compareelements)|(Statisch) Mit dieser Funktion können Sie zwei Elementen auf Gleichheit verglichen werden soll.|
|[CDefaultCompareTraits::CompareElementsOrdered](#compareelementsordered)|(Statisch) Rufen Sie diese Funktion, um das Element größer und kleiner zu bestimmen.|

## <a name="remarks"></a>Hinweise

Diese Klasse enthält zwei statische Funktionen zum Vergleichen von Elementen in einem Auflistungsobjekt-Klasse gespeichert. Diese Klasse wird verwendet, durch die [CDefaultElementTraits-Klasse](../../atl/reference/cdefaultelementtraits-class.md).

Weitere Informationen finden Sie unter [ATL-Auflistungsklassen](../../atl/atl-collection-classes.md).

## <a name="requirements"></a>Anforderungen

**Header:** atlcoll.h

##  <a name="compareelements"></a>  CDefaultCompareTraits::CompareElements

Mit dieser Funktion können Sie zwei Elementen auf Gleichheit verglichen werden soll.

```
static bool CompareElements(const T& element1, const T& element2);
```

### <a name="parameters"></a>Parameter

*Element1*<br/>
Das erste Element.

*Element2*<br/>
Das zweite Element.

### <a name="return-value"></a>Rückgabewert

Gibt "true" zurück, wenn die Elemente gleich "false", andernfalls sind.

### <a name="remarks"></a>Hinweise

Die Standardimplementierung dieser Funktion wird die Gleichheit (**==**) Operator. Diese Funktion müssen möglicherweise für Objekte, ausgenommen einfachen Datentypen außer Kraft gesetzt werden.

##  <a name="compareelementsordered"></a>  CDefaultCompareTraits::CompareElementsOrdered

Rufen Sie diese Funktion, um das Element größer und kleiner zu bestimmen.

```
static int CompareElementsOrdered(const T& element1, const T& element2);
```

### <a name="parameters"></a>Parameter

*Element1*<br/>
Das erste Element.

*Element2*<br/>
Das zweite Element.

### <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl, die anhand der folgenden Tabelle:

|Bedingung|Rückgabewert|
|---------------|------------------|
|*Element1* < *element2*|<0|
|*Element1* == *element2*|0|
|*Element1* > *element2*|>0|

### <a name="remarks"></a>Hinweise

Die Standardimplementierung dieser Funktion verwendet die **==**, **\<**, und **>** Operatoren. Diese Funktion müssen möglicherweise für Objekte, ausgenommen einfachen Datentypen außer Kraft gesetzt werden.

## <a name="see-also"></a>Siehe auch

[Übersicht über die Klasse](../../atl/atl-class-overview.md)
