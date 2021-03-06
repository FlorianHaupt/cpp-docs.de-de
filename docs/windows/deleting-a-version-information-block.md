---
title: Löschen eines Versionsinfoblockes (C++)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.version
helpviewer_keywords:
- blocks, deleting
- version information, deleting blocks
- resources [C++], deleting version information
ms.assetid: 4e1641eb-d5b2-4183-b273-bc5b51af1537
ms.openlocfilehash: e0bdc719e3ca3a3ffa4493f1d7c578a91733a7f3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50648304"
---
# <a name="deleting-a-version-information-block-c"></a>Löschen eines Versionsinfoblockes (C++)

### <a name="to-delete-a-version-information-block"></a>So löschen Sie einen Versionsinformationsblock

1. Öffnen Sie die Versionsinformationsressource, indem Sie in der [Ressourcenansicht](../windows/resource-view-window.md)auf ihr Symbol doppelklicken.

   > [!NOTE]
   > Wenn das Projekt noch keine RC-Datei enthält, informieren Sie sich unter [Erstellen einer neuen Ressourcenskriptdatei](../windows/how-to-create-a-resource-script-file.md).

2. Klicken Sie mit der rechten Maustaste auf den Blockheader, den Sie löschen möchten, und wählen Sie dann im Kontextmenü **Versionsinformationsblock löschen** aus.

   Mit diesem Befehl wird der ausgewählte Header gelöscht, die verbleibenden Versionsinformationen bleiben jedoch intakt. Beachten Sie, dass die Aktion nicht rückgängig gemacht werden kann.

Informationen zum Hinzufügen von Ressourcen zu verwalteten Projekten finden Sie unter [Ressourcen in Desktop-Apps](/dotnet/framework/resources/index) in die *(.NET Framework Developer's Guide*. Weitere Informationen zum manuellen Hinzufügen von Ressourcendateien zu verwalteten Projekten, den Zugriff auf Ressourcen, zum Anzeigen statischer Ressourcen und Zuweisen von Ressourcenzeichenfolgen zu Eigenschaften, finden Sie unter [Erstellen von Ressourcendateien für Desktop-Apps](/dotnet/framework/resources/creating-resource-files-for-desktop-apps). Weitere Informationen zur Globalisierung und Lokalisierung von Ressourcen in verwalteten apps finden Sie unter [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index).

## <a name="requirements"></a>Anforderungen

Win32

## <a name="see-also"></a>Siehe auch

[Versionsinfo-Editor](../windows/version-information-editor.md)<br/>
[Versionsinformationen (Windows)](https://msdn.microsoft.com/library/windows/desktop/ms646981.aspx)