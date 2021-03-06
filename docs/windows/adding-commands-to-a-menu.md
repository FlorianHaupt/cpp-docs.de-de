---
title: Hinzufügen von Befehlen zu einem Menü (C++)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.menu
helpviewer_keywords:
- menu items, adding to menus
- menus [C++], adding items
- commands [C++], adding to menus
ms.assetid: 1523a755-0ab5-42f8-9e98-bb9881564431
ms.openlocfilehash: 71a3a13b3c86fa4a4238fd9a42dd45b48ef318de
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50571417"
---
# <a name="adding-commands-to-a-menu-c"></a>Hinzufügen von Befehlen zu einem Menü (C++)

### <a name="to-add-commands-to-a-menu"></a>So fügen Sie Befehle zu einem Menü hinzu

1. [Erstellen Sie ein Menüelement](../windows/creating-a-menu.md).

2. Klicken Sie z. B. auf einen Menünamen, **Datei**.

   Jedes Menü wird erweitert, und es wird ein neues Elementfeld für Befehle zur Verfügung gestellt. Sie können z. B. die Befehle hinzufügen **neu**, **öffnen**, und **schließen** auf eine **Datei** Menü.

3. Geben Sie im neuen Elementfeld einen Namen für den neuen Menübefehl ein.

   > [!NOTE]
   > Der eingegebene Text wird sowohl im **Menü** -Editor als auch im Feld **Beschriftung** im [Eigenschaftenfenster](/visualstudio/ide/reference/properties-window)angezeigt. Die Eigenschaften des neuen Menüs können an einer der beiden Stellen bearbeitet werden.

   > [!TIP]
   > Sie können eine mnemonische Taste (Zugriffstaste) definieren, die dem Benutzer ermöglicht, den Menübefehl auszuwählen. Geben Sie ein kaufmännisches und-Zeichen (`&`) vor einen Buchstaben ein, um ihn als mnemonisch anzugeben. Der Benutzer kann den Menübefehl auswählen, indem er diesen Buchstaben eingibt.

4. In der **Eigenschaften** wählen Sie im Fenster Eigenschaften, die gelten für den Menübefehl. Weitere Informationen finden Sie unter [Menübefehlseigenschaften](../windows/menu-command-properties.md).

5. In der **Eingabeaufforderung** im Feld der **Eigenschaften** Fenster, geben Sie die eingabeaufforderungs-Zeichenfolge in der Statusleiste Ihrer Anwendung angezeigt werden sollen.

   Dadurch wird ein Eintrag mit einem Ressourcenbezeichner in der Zeichenfolgentabelle erstellt, der dem von Ihnen erstellten Menübefehl entspricht.

   > [!NOTE]
   > Eingabeaufforderungen können nur auf Menüelemente mit Anwenden einer **Popup** Eigenschaft **"true"**. Beispielsweise können Menüelemente auf oberster Ebene über Eingabeaufforderungen verfügen, wenn sie über Untermenüelemente verfügen. Der Zweck einer **Eingabeaufforderung** besteht darin anzugeben, was passiert, wenn ein Benutzer das Menüelement klickt.

6. Drücken Sie **EINGABETASTE** auf den Menübefehl abzuschließen.

   Das neue Elementfeld wird ausgewählt, sodass Sie zusätzliche Menübefehle erstellen können.

## <a name="requirements"></a>Anforderungen

Win32

## <a name="see-also"></a>Siehe auch

[Menü-Editor](../windows/menu-editor.md)