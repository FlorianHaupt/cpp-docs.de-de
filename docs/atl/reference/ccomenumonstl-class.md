---
title: CComEnumOnSTL-Klasse
ms.date: 11/04/2016
f1_keywords:
- CComEnumOnSTL
- atlcom/ATL::CComEnumOnSTL
helpviewer_keywords:
- CComEnumOnSTL class
ms.assetid: befe1a44-7a00-4f28-9a2e-cc0fa526643c
ms.openlocfilehash: 7b1efb3bd574edde59f6d8845d73a51dfabea433
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50626615"
---
# <a name="ccomenumonstl-class"></a>CComEnumOnSTL-Klasse

Diese Klasse definiert ein COM-Enumerator-Objekt auf Grundlage einer C++-Standardbibliothek-Auflistung.

## <a name="syntax"></a>Syntax

```
template <class Base,
    const IID* piid, class T, class Copy, class CollType, class ThreadModel = CComObjectThreadModel>
class ATL_NO_VTABLE CComEnumOnSTL : public IEnumOnSTLImpl<Base, piid,
T,
    Copy,
CollType>,
    public CComObjectRootEx<ThreadModel>
```

#### <a name="parameters"></a>Parameter

*Basis*<br/>
Ein COM-Enumerator. Finden Sie unter [IEnumString](/windows/desktop/api/objidl/nn-objidl-ienumstring) verdeutlicht.

*piid*<br/>
Ein Zeiger auf die Schnittstellen-ID der Enumeratorschnittstelle.

*T*<br/>
Der Typ des Elements, die von der Enumeratorschnittstelle verfügbar gemacht werden.

*Kopieren*<br/>
Ein [Richtlinie kopieren](../../atl/atl-copy-policy-classes.md) Klasse.

*CollType*<br/>
Eine C++-Standardbibliothek-Container-Klasse.

## <a name="remarks"></a>Hinweise

`CComEnumOnSTL` definiert ein COM-Enumerator-Objekt auf Grundlage einer C++-Standardbibliothek-Auflistung. Diese Klasse kann verwendet werden, allein oder zusammen mit [ICollectionOnSTLImpl](../../atl/reference/icollectiononstlimpl-class.md). Typische Schritte bei der Verwendung dieser Klasse werden im folgenden beschrieben. Weitere Informationen finden Sie unter [ATL-Auflistungen und-Enumerationen](../../atl/atl-collections-and-enumerators.md).

## <a name="to-use-this-class-with-icollectiononstlimpl"></a>So verwenden diese Klasse mit ICollectionOnSTLImpl:

- **TypeDef** eine Spezialisierung dieser Klasse.

- Verwenden der **Typedef** als das abschließende Vorlagenargument in einer Spezialisierung von `ICollectionOnSTLImpl`.

Finden Sie unter [ATL-Auflistungen und-Enumerationen](../../atl/atl-collections-and-enumerators.md) verdeutlicht.

## <a name="to-use-this-class-independently-of-icollectiononstlimpl"></a>So verwenden Sie diese Klasse unabhängig von ICollectionOnSTLImpl:

- **TypeDef** eine Spezialisierung dieser Klasse.

- Verwenden der **Typedef** als Vorlagenargument in einer Spezialisierung von `CComObject`.

- Erstellen Sie eine Instanz von der `CComObject` Spezialisierung.

- Initialisieren Sie das Enumeratorobjekt durch Aufrufen [IEnumOnSTLImpl::Init](../../atl/reference/ienumonstlimpl-class.md#init).

- Die Enumeratorschnittstelle an den Client zurückgeben.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

`CComObjectRootBase`

`Base`

[CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)

[IEnumOnSTLImpl](../../atl/reference/ienumonstlimpl-class.md)

`CComEnumOnSTL`

## <a name="requirements"></a>Anforderungen

**Header:** atlcom.h

## <a name="example"></a>Beispiel

Der folgenden Code stellt eine generische Funktion, um die Erstellung und Initialisierung eines Objekts Enumerator zu behandeln:

[!code-cpp[NVC_ATL_COM#34](../../atl/codesnippet/cpp/ccomenumonstl-class_1.h)]

Diese Vorlagenfunktion kann zum Implementieren der `_NewEnum` Eigenschaft einer Auflistung-Schnittstelle, wie unten dargestellt:

[!code-cpp[NVC_ATL_COM#35](../../atl/codesnippet/cpp/ccomenumonstl-class_2.h)]

Dieser Code erstellt eine **Typedef** für `CComEnumOnSTL` , verfügbar macht, einen Vektor von `CComVariant`s von der `IEnumVariant` Schnittstelle. Die `CVariantCollection` Klasse einfach spezialisiert `CreateSTLEnumerator` zum Arbeiten mit Objekten der Enumerator dieses Typs.

## <a name="see-also"></a>Siehe auch

[IEnumOnSTLImpl](../../atl/reference/ienumonstlimpl-class.md)<br/>
[-Beispiel: Demonstriert wird, ICollectionOnSTLImpl und CComEnumOnSTL benutzerdefinierten Kopierrichtlinienklassen](../../visual-cpp-samples.md)<br/>
[Übersicht über die Klasse](../../atl/atl-class-overview.md)<br/>
[CComObjectRootEx-Klasse](../../atl/reference/ccomobjectrootex-class.md)<br/>
[CComObjectThreadModel](atl-typedefs.md#ccomobjectthreadmodel)<br/>
[IEnumOnSTLImpl-Klasse](../../atl/reference/ienumonstlimpl-class.md)
