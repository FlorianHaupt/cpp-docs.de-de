---
title: 'Gewusst wie: Senden einer Nachricht in regelmäßigen Intervallen'
ms.date: 11/04/2016
helpviewer_keywords:
- timer class, example
- sending messages at regular intervals [Concurrency Runtime]
ms.assetid: 4b60ea6c-97c8-4d69-9f7b-ad79f3548026
ms.openlocfilehash: 05777b0c00f587f588a50733d5113d9a7362d247
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50549616"
---
# <a name="how-to-send-a-message-at-a-regular-interval"></a>Gewusst wie: Senden einer Nachricht in regelmäßigen Intervallen

Dieses Beispiel zeigt, wie Sie mit der Concurrency::[Timer-Klasse](../../parallel/concrt/reference/timer-class.md) zum Senden einer Nachricht in regelmäßigen Intervallen.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird während eines längeren Vorgangs der Status mithilfe eines `timer`-Objekts angezeigt. Dieses Beispiel verweist der `timer` -Objekt an eine [Concurrency:: Call](../../parallel/concrt/reference/call-class.md) Objekt. Das `call`-Objekt gibt in regelmäßigen Intervallen an der Konsole eine Statusanzeige aus. Die [Concurrency::timer::start](reference/timer-class.md#start) -Methode führt den Timer in einem separaten Kontext. Die `perform_lengthy_operation` Funktionsaufrufe der [Concurrency:: wait](reference/concurrency-namespace-functions.md#wait) Funktion in der main-Kontext, der einen zeitaufwändigen Vorgang zu simulieren.

[!code-cpp[concrt-report-progress#1](../../parallel/concrt/codesnippet/cpp/how-to-send-a-message-at-a-regular-interval_1.cpp)]

Dieses Beispiel erzeugt die folgende Beispielausgabe:

```Output
Performing a lengthy operation..........done.
```

## <a name="compiling-the-code"></a>Kompilieren des Codes

Kopieren Sie den Beispielcode und fügen Sie ihn in ein Visual Studio-Projekt, oder fügen Sie ihn in eine Datei mit dem Namen `report-progress.cpp` und führen Sie dann den folgenden Befehl in einem Fenster von Visual Studio-Eingabeaufforderung.

**CL.exe/EHsc Report-progress.cpp**

## <a name="see-also"></a>Siehe auch

[Asynchrone Agents Library](../../parallel/concrt/asynchronous-agents-library.md)<br/>
[Asynchrone Nachrichtenblöcke](../../parallel/concrt/asynchronous-message-blocks.md)<br/>
[Funktionen zum Übergeben von Nachrichten](../../parallel/concrt/message-passing-functions.md)
