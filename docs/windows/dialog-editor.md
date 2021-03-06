---
title: Dialog-Editor (C++)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.dialog.dialog
- vc.editors.dialog.F1
helpviewer_keywords:
- resource editors [C++], Dialog editor
- editors, dialog boxes
- Dialog editor
- dialog boxes [C++], editing
ms.assetid: d94884ef-2cca-49d8-9b58-775f34848134
ms.openlocfilehash: 9ca532e1691a5d92280c89067a943b7d2e27e3f6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50540880"
---
# <a name="dialog-editor-c"></a>Dialog-Editor (C++)

Die **Dialogfeld** -Editor können Sie zum Erstellen oder Bearbeiten von Dialogfeldressourcen. Sie öffnen den Dialog-Editor durch Doppelklicken auf ein Dialogfeld für die RC-Datei in die **Ressourcenansicht** Fenster (**Ansicht** > **Ressourcenansicht**). Beachten Sie, dass **Ressourcenansicht** ist in Express-Editionen nicht verfügbar.

Einer der ersten Schritte beim Erstellen eines neuen Dialogfelds (oder einer Dialogfeldvorlage) ist das Hinzufügen von Steuerelementen zum Dialogfeld. In der **Dialogfeld** -Editor, ordnen Sie Steuerelemente entsprechend einer bestimmten Größe, Form oder Ausrichtung, oder Sie verschieben sie rund um die Arbeit in das Dialogfeld. Steuerelemente lassen sich darüber hinaus problemlos löschen.

Um ein Dialogfeld später wiederzuverwenden, können Sie es als Vorlage speichern. Auch das Wechseln zwischen dem Entwurf des Dialogfelds und dem Bearbeiten des Codes, mit dem das Feld implementiert wird, ist denkbar einfach.

Der Dialog-Editor bietet zusätzlich die Möglichkeit, die Eigenschaften einzelner oder mehrerer Steuerelemente zu bearbeiten. Sie können die Aktivierreihenfolge ändern, d. h. die Reihenfolge an, bei dem Steuerelemente erhalten, Fokus, wenn die **Registerkarte** gedrückt wird, oder Sie definieren eine Zugriffstaste (Tastenkombination), die Benutzern ermöglicht, wählen Sie ein Steuerelement unter Verwendung der Tastaturfokus. Eine Liste der vordefinierten Zugriffstasten finden Sie unter [Zugriffstasten für den Dialog-Editor](../windows/accelerator-keys-for-the-dialog-editor.md).

Die **Dialogfeld** Editor ermöglicht auch das Ihnen die Verwendung benutzerdefinierter Steuerelemente einschließlich ActiveX-Steuerelemente. Außerdem können [Formularansichten](../mfc/reference/cformview-class.md), [Datensatzansichten](../data/record-views-mfc-data-access.md)oder [Dialogleisten](../mfc/dialog-bars.md)bearbeitet werden.

Ab Visual Studio 2015 wird können den Dialog-Editor Sie dynamische Layouts definieren, die angeben, wie Sie Steuerelemente zum Verschieben und anpassen, wenn der Benutzer die Größe eines Dialogfelds ändert. Weitere Informationen finden Sie unter [Dynamic Layout](../mfc/dynamic-layout.md).

- [Erstellen eines neuen Dialogfelds](../windows/creating-a-new-dialog-box.md)

- [Erstellen eines Dialogfelds, das zur Laufzeit vom Benutzer nicht beendet werden kann](../windows/creating-a-dialog-box-that-users-cannot-exit.md)

- [Ein- oder Ausblenden der Symbolleiste des Dialog-Editors](../windows/showing-or-hiding-the-dialog-editor-toolbar.md)

- [Umschalten zwischen Dialogfeld-Editor und Code](../windows/switching-between-dialog-box-controls-and-code.md)

- [Steuerelemente in Dialogfeldern](../windows/controls-in-dialog-boxes.md)

- [Hinzufügen von Ereignishandlern für Dialogfeld-Steuerelemente](../windows/adding-event-handlers-for-dialog-box-controls.md)

- [Testen eines Dialogfelds](../windows/testing-a-dialog-box.md)

- [Zugriffstasten für den Dialog-Editor](../windows/accelerator-keys-for-the-dialog-editor.md)

- [Problembehandlung beim Dialog-Editor](../windows/troubleshooting-the-dialog-editor.md)

   > [!TIP]
   > Bei der Verwendung der **Dialogfeld** -Editor in vielen Fällen können Sie die rechte Maustaste gedrückt, um ein Kontextmenü mit häufig verwendeten Befehlen anzuzeigen klicken.

Informationen zum Hinzufügen von Ressourcen zu verwalteten Projekten finden Sie unter [Ressourcen in Desktop-Apps](/dotnet/framework/resources/index) in die *(.NET Framework Developer's Guide*. Weitere Informationen zum manuellen Hinzufügen von Ressourcendateien zu verwalteten Projekten, den Zugriff auf Ressourcen, zum Anzeigen statischer Ressourcen und Zuweisen von Ressourcenzeichenfolgen zu Eigenschaften, finden Sie unter [Erstellen von Ressourcendateien für Desktop-Apps](/dotnet/framework/resources/creating-resource-files-for-desktop-apps). Weitere Informationen zur Globalisierung und Lokalisierung von Ressourcen in verwalteten apps finden Sie unter [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index).

## <a name="requirements"></a>Anforderungen

Win32

## <a name="see-also"></a>Siehe auch

[Ressourcen-Editor](../windows/resource-editors.md)<br/>
[Steuerelemente](../mfc/controls-mfc.md)<br/>
[Steuerelementklassen](../mfc/control-classes.md)<br/>
[Dialogfeldklassen](../mfc/dialog-box-classes.md)<br/>
[Dialogfeld-Steuerelemente und Variablentypen](../ide/dialog-box-controls-and-variable-types.md)