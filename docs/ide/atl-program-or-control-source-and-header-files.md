---
title: ATL-Programm oder Steuern von Quell- und Headerdateien
ms.date: 11/04/2016
helpviewer_keywords:
- file types [C++], ATL source and headers
ms.assetid: cb65372f-4880-4007-b582-a52eaa568fd1
ms.openlocfilehash: dc2fc7a81d2d32e6bc89e1c10b8fe090650db2ec
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50630580"
---
# <a name="atl-program-or-control-source-and-header-files"></a>ATL-Programm oder Steuern von Quell- und Headerdateien

Folgende Dateien werden abhängig von den ausgewählten Optionen für das Projekt erstellt, wenn Sie ein ATL-Projekt in Visual Studio erstellen.

Diese Dateien befinden Sich alle im Verzeichnis *Projname*. Im Projektmappen-Explorer befinden diese sich entweder im Ordner „Headerdateien“ (H-Dateien) oder im Ordner „Quelldateien“ (CPP-Dateien).

|Dateiname|Beschreibung |
|---------------|-----------------|
|*Projname*.h|Die Hauptincludedatei, die die C++-Schnittstellendefinitionen und GUID-Deklarationen der in der Datei „ATLSample.idl“ definierten Elemente enthält. Sie wird während der Kompilierung von MIDL erneut generiert.|
|*Projname*.cpp|Die Quelldatei des Hauptprogramms. Sie enthält die Implementierung der Exporte für einen In-Process-Server Ihrer DLL und die Implementierung von `WinMain` für einen lokalen Server. Für einen Dienst implementiert sie zusätzlich alle Dienstverwaltungsoptionen.|
|Resource.h|Die Headerdatei für die Ressourcendatei|
|StdAfx.cpp|Enthält die Dateien „StdAfx.h“ und „Atlimpl.cpp“.|
|StdAfx.h|Enthält die ATL-Headerdateien.|

## <a name="see-also"></a>Siehe auch

[Für Visual C++-Projekte erstellte Dateitypen](../ide/file-types-created-for-visual-cpp-projects.md)<br>
[MFC-Programm oder Steuern von Quell- und Headerdateien](../ide/mfc-program-or-control-source-and-header-files.md)<br>
[CLR Projects (CLR-Projekte)](../ide/files-created-for-clr-projects.md)