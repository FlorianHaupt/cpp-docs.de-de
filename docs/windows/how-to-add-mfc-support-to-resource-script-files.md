---
title: 'Vorgehensweise: Hinzufügen von MFC-Unterstützung zu Ressourcenskriptdateien (C++)'
ms.date: 11/04/2016
f1_keywords:
- vc.resvw.add.MFC
helpviewer_keywords:
- rc files [C++], adding MFC support
- .rc files [C++], adding MFC support
- MFC, adding support to resource scripts files
- resource script files [C++], adding MFC support
ms.assetid: 599dfe9d-ad26-4e34-899c-49b56599e37f
ms.openlocfilehash: c2d0f9ee30085bd2bcc02cf48fd18f6de63eb69a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50594388"
---
# <a name="how-to-add-mfc-support-to-resource-script-files-c"></a>Vorgehensweise: Hinzufügen von MFC-Unterstützung zu Ressourcenskriptdateien (C++)

In der Regel beim Erstellen einer MFC-Anwendung für die Verwendung von Windows die [MFS-Anwendungsassistenten](../mfc/reference/mfc-application-wizard.md), der Assistent generiert eine Reihe grundlegende Dateien (einschließlich einer Ressourcenskriptdatei (.rc)), das die Kernfunktionen von Microsoft Foundation enthält. Klassen (MFC). Wenn Sie jedoch eine RC-Datei für eine Windows-Anwendung bearbeiten, die nicht auf MFC basiert, sind die folgenden, für die MFC-Grundstruktur spezifischen Funktionen nicht verfügbar:

- MFC-Code-Assistenten

- Zeichenfolgen für Menüaufforderungen

- Auflisten der Inhalte von Kombinationsfeld-Steuerelementen

- Hosting von ActiveX-Steuerelementen

Vorhandenen RC-Dateien, die noch nicht über MFC-Unterstützung verfügen, kann diese jedoch hinzugefügt werden.

### <a name="to-add-mfc-support-to-rc-files"></a>So fügen Sie RC-Dateien MFC-Unterstützung hinzu

1. Öffnen Sie die Ressourcenskriptdatei.

   > [!NOTE]
   > Wenn das Projekt noch keine RC-Datei enthält, informieren Sie sich unter [Erstellen einer neuen Ressourcenskriptdatei](../windows/how-to-create-a-resource-script-file.md).

2. In [Ressourcenansicht](../windows/resource-view-window.md), markieren Sie den Ordner "Resources" (z. B. MFC.rc).

3. In der [Fenster "Eigenschaften"](/visualstudio/ide/reference/properties-window)legen die **MFC Mode** Eigenschaft **"true"**.

   > [!NOTE]
   > Zusätzlich zum Festlegen dieses Flags muss auch gewährleistet sein, dass die RC-Datei Teil eines MFC-Projekts ist. Festlegen von z. B. nur **MFC Mode** zu **"true"** auf eine RC-Datei in eine Win32-Projekt wird nicht Geben Sie die MFC-Features.

## <a name="requirements"></a>Anforderungen

MFC

## <a name="see-also"></a>Siehe auch

[Ressourcendateien](../windows/resource-files-visual-studio.md)<br/>
[Ressourcen-Editor](../windows/resource-editors.md)