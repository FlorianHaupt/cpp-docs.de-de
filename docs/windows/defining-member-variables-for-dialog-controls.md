---
title: Definieren von Membervariablen für Dialogfeld-Steuerelemente (C++)
ms.date: 11/04/2016
helpviewer_keywords:
- member variables, defining for controls
- variables, dialog box control member variables
- controls [C++], member variables
- Dialog Editor [C++], defining member variables for controls
ms.assetid: 84347c63-c33c-4b04-91f5-6d008c45ba58
ms.openlocfilehash: 56a7d01d26656c8cf9def3bf09e3ccb18fb436fd
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50449454"
---
# <a name="defining-member-variables-for-dialog-controls-c"></a>Definieren von Membervariablen für Dialogfeld-Steuerelemente (C++)

Mit der folgenden Methode können Sie eine Membervariable für beliebige Dialogfenster-Steuerelemente außer Schaltflächen definieren.

> [!NOTE]
> Dieser Artikel gilt nur für Dialogfeld-Steuerelemente innerhalb eines MFC-Projekts. ATL-Projekte verwenden, sollten die **neue Windows-Meldungen und Ereignishandler** Dialogfeld.

### <a name="to-define-a-member-variable-for-a-non-button-dialog-box-control"></a>So definieren Sie eine Membervariable für ein Dialogfeld-Steuerelement (kein Schaltflächen-Steuerelement)

1. In der [Dialog-Editor](../windows/dialog-editor.md), wählen Sie ein Steuerelement.

2. Beim Drücken der **STRG** Schlüssel, doppelklicken Sie auf das Dialogfeld-Steuerelement.

   Die [Assistenten zum Hinzufügen von Membervariablen](../ide/add-member-variable-wizard.md) angezeigt wird.

3. Geben Sie die entsprechende Informationen in den **Hinzufügen von Membervariablen** Assistenten. Weitere Informationen finden Sie unter [Dialogdatenaustausch](../mfc/dialog-data-exchange.md).

4. Klicken Sie auf **OK** zum Zurückgeben der **Dialogfeld** Editor.

   > [!TIP]
   > Doppelklicken Sie auf das Steuerelement, um von einem Dialogfeld-Steuerelement zu seinem vorhandenen Handler zu wechseln.

Sie können auch die **Membervariablen** Registerkarte **MFC-Klassenassistent** neue Membervariablen für eine angegebene Klasse hinzufügen und anzeigen, die bereits definiert wurden.

## <a name="requirements"></a>Anforderungen

MFC

## <a name="see-also"></a>Siehe auch

[Zuordnen von Meldungen zu Funktionen](../mfc/reference/mapping-messages-to-functions.md)<br/>
[Adding Functionality with Code Wizards (Hinzufügen neuer Funktionen mit Code-Assistenten)](../ide/adding-functionality-with-code-wizards-cpp.md)<br/>
[MFC-Klassen-Assistent](../mfc/reference/mfc-class-wizard.md)<br/>
[Hinzufügen einer Klasse](../ide/adding-a-class-visual-cpp.md)<br/>
[Hinzufügen einer Memberfunktion](../ide/adding-a-member-function-visual-cpp.md)<br/>
[Adding a Member Variable (Hinzufügen einer Membervariablen)](../ide/adding-a-member-variable-visual-cpp.md)<br/>
[Überschreiben einer virtuellen Funktion](../ide/overriding-a-virtual-function-visual-cpp.md)<br/>
[MFC Message Handler (MFC-Meldungshandler)](../mfc/reference/adding-an-mfc-message-handler.md)