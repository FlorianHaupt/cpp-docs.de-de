---
title: IPropertyNotifySinkCP-Klasse
ms.date: 11/04/2016
f1_keywords:
- IPropertyNotifySinkCP
- atlctl/ATL::IPropertyNotifySinkCP
helpviewer_keywords:
- connection points [C++], managing
- sinks, notifying of changes
- IPropertyNotifySinkCP class
ms.assetid: 1b41445e-bc88-4fa6-bb62-d68aacec2bd5
ms.openlocfilehash: 6a80ff17b5d8083704b144686d8bff27be115b18
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50461606"
---
# <a name="ipropertynotifysinkcp-class"></a>IPropertyNotifySinkCP-Klasse

Diese Klasse stellt [IPropertyNotifySink](/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink) Schnittstelle als Ausgangsschnittstelle auf einem verbindungsfähigen Objekt.

> [!IMPORTANT]
>  Diese Klasse und ihre Member können nicht in Anwendungen verwendet werden, die in der Windows-Runtime ausgeführt werden.

## <a name="syntax"></a>Syntax

```
template<class T, class CDV = CComDynamicUnkArray>
class IPropertyNotifySinkCP
   : public IConnectionPointImpl<T, &IID_IPropertyNotifySink, CDV>
```

#### <a name="parameters"></a>Parameter

*T*<br/>
Abgeleitet von die Klasse `IPropertyNotifySinkCP`.

*CDV*<br/>
Eine Klasse, die Verbindungen zwischen einem Verbindungspunkt und die senken verwaltet. Der Standardwert ist [CComDynamicUnkArray](../../atl/reference/ccomdynamicunkarray-class.md), womit unbegrenzte Verbindungen. Sie können auch [CComUnkArray](../../atl/reference/ccomunkarray-class.md), die eine feste Anzahl von Verbindungen angibt.

## <a name="remarks"></a>Hinweise

`IPropertyNotifySinkCP` erbt alle Methoden über seine Basisklasse, [IConnectionPointImpl](../../atl/reference/iconnectionpointimpl-class.md).

Die [IPropertyNotifySink](/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink) Schnittstelle ermöglicht es einem Senkenobjekts zum Empfangen von Benachrichtigungen über eigenschaftsänderungen. Klasse `IPropertyNotifySinkCP` macht diese Schnittstelle als Ausgangsschnittstelle auf einem verbindungsfähigen Objekt verfügbar. Der Client implementieren muss die `IPropertyNotifySink` Methoden für die Senke.

Leiten Sie eine Klasse von `IPropertyNotifySinkCP` Wenn Sie einen Verbindungspunkt erstellen, das darstellt möchten die `IPropertyNotifySink` Schnittstelle.

Weitere Informationen zur Verwendung von Verbindungspunkten in ATL finden Sie im Artikel [Verbindungspunkte](../../atl/atl-connection-points.md).

## <a name="requirements"></a>Anforderungen

**Header:** atlctl.h

## <a name="see-also"></a>Siehe auch

[IConnectionPointImpl-Klasse](../../atl/reference/iconnectionpointimpl-class.md)<br/>
[IConnectionPointContainerImpl-Klasse](../../atl/reference/iconnectionpointcontainerimpl-class.md)<br/>
[Übersicht über die Klasse](../../atl/atl-class-overview.md)
