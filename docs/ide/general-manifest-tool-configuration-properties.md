---
title: Konfigurationseigenschaften des Manifesttools (Visual C++)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCManifestTool.MergeRulesFile
- VC.Project.VCManifestTool.UseUnicodeResponseFiles
- VC.Project.VCManifestTool.SuppressStartupBanner
- VC.Project.VCManifestTool.UseFAT32Workaround
- VC.Project.VCManifestTool.VerboseOutput
- VC.Project.VCManifestTool.AssemblyIdentity
ms.assetid: b99368a5-6819-482c-a06e-f2409290cfd1
ms.openlocfilehash: 5706a67ac3f6be7a916d6f4f0ee8ccfafdfb9475
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50565216"
---
# <a name="general-manifest-tool-configuration-properties-ltprojectnamegt-property-pages-dialog-box"></a>Allgemein, Manifesttool, Konfigurationseigenschaften, Dialogfeld „&lt;Projektname&gt;-Eigenschaftenseiten“

Verwenden Sie dieses Dialogfeld, um allgemeine Optionen für die Datei [Mt.exe](https://msdn.microsoft.com/library/aa375649) anzugeben.

Öffnen Sie die Eigenschaftenseiten für Ihr Projekt oder Ihr Eigenschaftenblatt, um auf das Dialogfeld „Eigenschaftenseite“ zuzugreifen. Erweitern Sie den Knoten **Manifesttool** unter **Konfigurationseigenschaften**, und klicken Sie dann auf **Allgemein**.

## <a name="uielement-list"></a>UIElement-Liste

- **Startbanner unterdrücken**

   **Ja (/nologo)** gibt an, dass standardmäßige Copyrightinformationen von Microsoft beim Starten des Manifesttools ausgeblendet werden. Verwenden Sie diese Option, um unerwünschte Ausgabe in Protokolldateien zu unterdrücken, wenn Sie die „mt.exe“ als Teil eines Buildprozesses oder in einer Buildumgebung ausführen.

- **Ausführliche Ausgabe**

   **Ja (/verbose)** gibt an, dass zusätzliche Buildinformationen während der Manifestgenerierung angezeigt werden.

- **Assemblyidentität**

   Verwendet die Option „/identity“, um eine Identitätszeichenfolge anzugeben, die aus den Attributen für das [\<assemblyIdentity>-Element](/visualstudio/deployment/assemblyidentity-element-clickonce-application) besteht. Eine Identitätszeichenfolge beginnt mit dem Wert für das `name`-Attribut gefolgt von *Attribut* = *Wert*-Paaren. Die Attribute in einer Identitätszeichenfolge werden durch Kommas getrennt.

   Im Folgenden finden Sie eine Beispielidentitätszeichenfolge:

   `Microsoft.Windows.Common-Controls, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=6595b64144ccf1df`

## <a name="see-also"></a>Siehe auch

[ClickOnce Application Manifest](/visualstudio/deployment/clickonce-application-manifest)<br>
[Manifesttool-Eigenschaftenseiten](../ide/manifest-tool-property-pages.md)<br>
[Arbeiten mit Projekteigenschaften](../ide/working-with-project-properties.md)