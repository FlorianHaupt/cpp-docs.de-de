---
title: 1. Einführung
ms.date: 11/04/2016
ms.assetid: c42e72bc-0e31-4b1c-b670-cd82673c0c5a
ms.openlocfilehash: b365ff828fd7dc2b7d9d3136a4fbfb68c43902ce
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50554712"
---
# <a name="1-introduction"></a>1. Einführung

Dieses Dokument beschreibt eine Auflistung von Compiler-Direktiven, Bibliotheksfunktionen und Umgebungsvariablen, die verwendet werden können, um shared Memory-Parallelität in C und C++-Programmen anzugeben. Die in diesem Dokument beschriebene Funktionen werden zusammen als bezeichnet die *OpenMP C/C++-Anwendung die API (Anwendungsprogrammierschnittstelle)*. Das Ziel dieser Spezifikation kann ein Modell bereitstellen, für die parallele Programmierung, die ein Programm über das shared Memory-Architekturen von unterschiedlichen Herstellern portabel sein. OpenMP C-/C++-API wird vom Compiler von vielen Anbietern unterstützt werden. Weitere Informationen zu OpenMP, einschließlich der *OpenMP Fortran Anwendungsprogrammierschnittstelle*, finden Sie unter der folgenden Website:

[http://www.openmp.org](http://www.openmp.org)

Die Direktiven Bibliotheksfunktionen und Umgebungsvariablen, die in diesem Dokument können Benutzer zum Erstellen und Verwalten von parallelen Programmen zugleich Portabilität. Erweitern Sie die Anweisungen des C und C++ sequenzielle Programmierungsmodells mit single-Program mehrere Datenkonstrukte (SPMD) Arbeitsteilungskonstrukte und Synchronisierungskonstrukten und bieten Unterstützung für die gemeinsame Nutzung und Privatisierung von Daten. Compiler, die der OpenMP-C- und C++-API unterstützen, werden eine Befehlszeilenoption für den Compiler enthalten, die aktiviert und ermöglicht die Darstellung alle OpenMP Compilerdirektiven.