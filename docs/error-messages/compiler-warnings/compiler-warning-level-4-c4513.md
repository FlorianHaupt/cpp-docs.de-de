---
title: Compilerwarnung (Stufe 4) C4513
ms.date: 11/04/2016
f1_keywords:
- C4513
helpviewer_keywords:
- C4513
ms.assetid: 6877334a-f30a-4184-9483-dac3348737a4
ms.openlocfilehash: cbde035a988e5f6ac64303b2ed159b885ece8684
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50520076"
---
# <a name="compiler-warning-level-4-c4513"></a>Compilerwarnung (Stufe 4) C4513

'Klasse': Destruktor konnte nicht generiert werden

Der Compiler kann keinen Standarddestruktor für die angegebene Klasse generieren; Es wurde kein Destruktor erstellt. Der Destruktor ist in einer Basisklasse, die für die abgeleitete Klasse nicht zugänglich ist. Wenn die Basisklasse über einen privaten Destruktor verfügt, stellen sie öffentliche oder geschützte.