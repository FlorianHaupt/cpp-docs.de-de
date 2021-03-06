---
title: Hinzufügen einer lokalen Eigenschaft (Visual C++)
ms.date: 11/04/2016
helpviewer_keywords:
- interfaces, adding properties
- properties [C++], adding to interfaces
ms.assetid: 37bd4db7-efd3-4faa-87ad-64902ed16a36
ms.openlocfilehash: 3c47a5b50442f47e6042ea1232590dbdde7299ec
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50563084"
---
# <a name="adding-a-property-visual-c"></a>Hinzufügen einer lokalen Eigenschaft (Visual C++)

Sie können den [Assistenten zum Hinzufügen von Eigenschaften](../ide/names-add-property-wizard.md) verwenden, um einer Schnittstelle in Ihrem Projekt eine Eigenschaft hinzuzufügen.

### <a name="to-add-a-property-to-your-object"></a>So fügen Sie Ihrem Objekt eine Eigenschaft hinzu

1. Klicken Sie in der [Klassenansicht](/visualstudio/ide/viewing-the-structure-of-code) mit der rechten Maustaste auf den Namen der Schnittstelle, der die Eigenschaft hinzugefügt werden soll.

   > [!NOTE]
   > Sie können Eigenschaften auch zu Disp-Schnittstellen hinzufügen, die im Bibliotheksknoten geschachtelt sind, sofern das Projekt nicht attributiert ist.

1. Klicken Sie im Kontextmenü auf die Option **Hinzufügen**, und klicken Sie danach auf **Eigenschaft hinzufügen**.

1. Geben Sie im [Assistenten zum Hinzufügen von Eigenschaften](../ide/names-add-property-wizard.md) die Informationen zum Erstellen der Eigenschaft an.

1. Geben Sie alle Einstellungen der Interface Definiton Language dieser Eigenschaft auf der Seite [IDL-Attribute](../ide/idl-attributes-add-property-wizard.md) des Assistenten an.

1. Klicken Sie auf **Fertig stellen**, um die Eigenschaft hinzuzufügen.

Die Methoden **Get** und `Put` der Eigenschaft werden in der Klassenansicht als zwei Symbole unter der Schnittstelle angezeigt, in der sie definiert sind. Sie können eines der Symbole doppelklicken, um die Eigenschaftsdeklaration in der IDL-Datei anzuzeigen.

- Bei ATL-Schnittstellen werden die Funktionen **Get** und **Put** der CPP-Datei hinzugefügt, und Verweise auf diese Funktionen werden der H-Datei hinzugefügt.

- Wenn Sie bei MFC-Disp-Schnittstellen **Membervariable** als Implementierungstyp auswählen, werden der implementierenden Klasse eine Methode und eine Variable hinzugefügt. Wenn Sie die **Get/Set-Methoden** als Implementierungstyp auswählen, werden der implementierenden Klasse zwei Methoden hinzugefügt.

## <a name="see-also"></a>Siehe auch

[Erstellen einer COM-Schnittstelle](../ide/creating-a-com-interface-visual-cpp.md)<br>
[Bearbeiten einer COM-Schnittstelle](../ide/editing-a-com-interface.md)<br>
[Das Component Object Model](/windows/desktop/com/the-component-object-model)<br>
[Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)](/windows/desktop/com/interface-pointers-and-interfaces)