---
title: Compilerwarnung (Stufe 4) C4718
ms.date: 11/04/2016
f1_keywords:
- C4718
helpviewer_keywords:
- C4718
ms.assetid: 29507f8a-b024-42c1-a3b8-f35d1f2641f3
ms.openlocfilehash: c313e26af5f5b17db9c7d001a705ff7211461c2b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50573689"
---
# <a name="compiler-warning-level-4-c4718"></a>Compilerwarnung (Stufe 4) C4718

'Funktionsaufruf': Rekursiver Aufruf besitzt keine Nebeneffekte, wird gelöscht

Eine Funktion enthält einen rekursiven Aufruf, hat aber ansonsten keine Nebeneffekte. Ein Aufruf dieser Funktion wird gelöscht. Die Richtigkeit des Programms ist nicht betroffen, aber die Verhaltensweise. Wenn der Aufruf beibehalten wird, kann dies zu einer Stapelüberlaufausnahme zur Laufzeit führen. Das Löschen des Aufrufs beseitigt diese Möglichkeit.