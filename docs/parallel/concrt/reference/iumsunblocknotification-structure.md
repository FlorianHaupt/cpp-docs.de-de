---
title: IUMSUnblockNotification-Struktur
ms.date: 11/04/2016
f1_keywords:
- IUMSUnblockNotification
- CONCRTRM/concurrency::IUMSUnblockNotification
- CONCRTRM/concurrency::IUMSUnblockNotification::IUMSUnblockNotification::GetContext
- CONCRTRM/concurrency::IUMSUnblockNotification::IUMSUnblockNotification::GetNextUnblockNotification
helpviewer_keywords:
- IUMSUnblockNotification structure
ms.assetid: eaca9529-c1cc-472b-8ec6-722a1ff0fa2a
ms.openlocfilehash: 219e32cedb02d4ecab73390e33601de32f9b0992
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50677967"
---
# <a name="iumsunblocknotification-structure"></a>IUMSUnblockNotification-Struktur

Stellt eine Benachrichtigung vom Ressourcen-Manager darüber dar, dass ein Threadproxy, der blockiert und eine Rückkehr zum festgelegten Planungskontext des Planers ausgelöst hatte, die Blockierung aufgehoben hat und zum Planen bereit ist. Diese Schnittstelle ist ungültig, sobald der zugeordnete Ausführungskontext des Threadproxys, der von der `GetContext`-Methode zurückgegeben wurde, neu geplant wird.

## <a name="syntax"></a>Syntax

```
struct IUMSUnblockNotification;
```

## <a name="members"></a>Member

### <a name="public-methods"></a>Öffentliche Methoden

|Name|Beschreibung|
|----------|-----------------|
|[IUMSUnblockNotification::GetContext](#getcontext)|Gibt die `IExecutionContext` Schnittstelle für den Ausführungskontext der Threadproxy, der Blockierung aufgehoben hat zugeordnet. Nach Rückgabe dieser Methode und der zugrunde liegende Ausführungskontext neu geplant wurde, über einen Aufruf an die `IThreadProxy::SwitchTo` -Methode, die diese Schnittstelle ist nicht mehr gültig.|
|[IUMSUnblockNotification::GetNextUnblockNotification](#getnextunblocknotification)|Gibt die nächste `IUMSUnblockNotification` -Schnittstelle in der Kette, die von der Methode zurückgegebenen `IUMSCompletionList::GetUnblockNotifications`.|

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

`IUMSUnblockNotification`

## <a name="requirements"></a>Anforderungen

**Header:** concrtrm.h

**Namespace:** Parallelität

##  <a name="getcontext"></a>  IUMSUnblockNotification:: GetContext-Methode

Gibt die `IExecutionContext` Schnittstelle für den Ausführungskontext der Threadproxy, der Blockierung aufgehoben hat zugeordnet. Nach Rückgabe dieser Methode und der zugrunde liegende Ausführungskontext neu geplant wurde, über einen Aufruf an die `IThreadProxy::SwitchTo` -Methode, die diese Schnittstelle ist nicht mehr gültig.

```
virtual IExecutionContext* GetContext() = 0;
```

### <a name="return-value"></a>Rückgabewert

Ein `IExecutionContext` Schnittstelle für den Ausführungskontext für eine Threadproxy, der Blockierung aufgehoben hat.

##  <a name="getnextunblocknotification"></a>  IUMSUnblockNotification:: GetNextUnblockNotification-Methode

Gibt die nächste `IUMSUnblockNotification` -Schnittstelle in der Kette, die von der Methode zurückgegebenen `IUMSCompletionList::GetUnblockNotifications`.

```
virtual IUMSUnblockNotification* GetNextUnblockNotification() = 0;
```

### <a name="return-value"></a>Rückgabewert

Die nächste `IUMSUnblockNotification` -Schnittstelle in der Kette, die von der Methode zurückgegebenen `IUMSCompletionList::GetUnblockNotifications`.

## <a name="see-also"></a>Siehe auch

[Concurrency-Namespace](concurrency-namespace.md)<br/>
[IUMSScheduler-Struktur](iumsscheduler-structure.md)<br/>
[IUMSCompletionList-Struktur](iumscompletionlist-structure.md)
