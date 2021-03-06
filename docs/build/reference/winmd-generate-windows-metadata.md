---
title: /WINMD (Windows-Metadaten generieren)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.GenerateWindowsMetadata
ms.assetid: bcfb4901-411e-4c9e-9f78-23028b6e5fcc
ms.openlocfilehash: 3a59dd770d9429f23a4f401c6e1f5b13b9f743ef
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50656104"
---
# <a name="winmd-generate-windows-metadata"></a>/WINMD (Windows-Metadaten generieren)

Aktiviert die Generierung einer Windows-Runtime-Metadatendatei (.winmd)-Datei.

> **/ WINMD**\[**:**{**KEINE**\|**NUR**}]

## <a name="arguments"></a>Argumente

**/WINMD**<br/>
Die Standardeinstellung für die universelle Windows-Plattform-apps. Der Linker generiert sowohl die binäre ausführbare Datei als auch die winmd-Metadaten-Datei.

**/WINMD:NO**<br/>
Der Linker wird nur die binäre ausführbare Datei, aber nicht in eine winmd-Datei generiert.

**/ WINMD: NUR**<br/>
Der Linker wird nur die winmd-Datei, aber nicht die binäre ausführbare Datei generiert.

## <a name="remarks"></a>Hinweise

Die **/WINMD** -Linkeroption wird für UWP-apps und Windows-Runtime-Komponenten verwendet, um die Erstellung einer Windows-Runtime-Metadatendatei (.winmd) zu steuern. Eine winmd-Datei ist eine Art von DLL, die Metadaten für Windows-Runtime-Typen und im Fall von Runtime-Komponenten, die Implementierungen dieser Typen enthält. Die Metadaten folgen der [ECMA-335](http://www.ecma-international.org/publications/standards/Ecma-335.htm) standard.

Standardmäßig den Namen der Ausgabedatei hat das Format *Binaryname*winmd. Um einen anderen Dateinamen anzugeben, verwenden die [/winmdfile](../../build/reference/winmdfile-specify-winmd-file.md) Option.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Linkeroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Ausführliche Informationen finden Sie unter [Working with Project Properties (Arbeiten mit Projekteigenschaften)](../../ide/working-with-project-properties.md).

1. Wählen Sie die **Konfigurationseigenschaften** > **Linker** > **Windows-Metadaten** Eigenschaftenseite.

1. In der **Windows-Metadaten generieren** Dropdown-Liste Wählen Sie die gewünschte Option.

## <a name="see-also"></a>Siehe auch

[Exemplarische Vorgehensweise: Erstellen einer einfachen Windows-Runtime-Komponente, und es über JavaScript aufrufen](/windows/uwp/winrt-components/walkthrough-creating-a-simple-windows-runtime-component-and-calling-it-from-javascript)<br/>
[Einführung in die Microsoft Interface Definition Language 3.0](/uwp/midl-3/intro)<br/>
[/WINMDFILE (WINMD-Datei angeben)](winmdfile-specify-winmd-file.md)<br/>
[/WINMDKEYFILE (WINMD-Schlüsseldatei angeben)](winmdkeyfile-specify-winmd-key-file.md)<br/>
[/WINMDKEYCONTAINER (Schlüsselcontainer angeben)](winmdkeycontainer-specify-key-container.md)<br/>
[/WINMDDELAYSIGN (WINMD-Datei teilweise signieren)](winmddelaysign-partially-sign-a-winmd.md)<br/>
[Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)<br/>
[Linkeroptionen](../../build/reference/linker-options.md)
