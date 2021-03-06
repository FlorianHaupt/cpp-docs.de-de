---
title: Zwischenablage
ms.date: 11/04/2016
helpviewer_keywords:
- cutting and copying data
- copying data
- Clipboard
- Clipboard, programming
- transferring data
ms.assetid: a71b2824-1f14-4914-8816-54578d73ad4e
ms.openlocfilehash: b17268c78fb5e82cbe75cbe0647b931d06934ef1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50440793"
---
# <a name="clipboard"></a>Zwischenablage

In dieser Artikelreihe wird erläutert, wie Unterstützung für die Windows-Zwischenablage in MFC-Anwendungen implementieren. Die Windows-Zwischenablage wird auf zwei Arten verwendet:

- Implementierende standard Befehle im Menü Bearbeiten, z. B. Ausschneiden, kopieren und einfügen.

- Uniform Data implementieren, übertragen Sie mit Drag und drop (OLE).

Die Zwischenablage ist die standard-Windows-Methode der Übertragung von Daten zwischen einer Quelle und Ziel. Es kann auch in OLE-Operationen sehr nützlich sein. Durch die Einführung von OLE gibt es zwei Mechanismen der Zwischenablage in Windows. Der standardmäßigen Windows-Zwischenablage-API ist weiterhin verfügbar, aber es wurde mit der OLE-Datenübertragungsmechanismus ergänzt wurde. OLE einheitliche Datenübertragung (UDT) unterstützt, Ausschneiden, kopieren und Einfügen über die Zwischenablage, und ziehen und ablegen.

Die Zwischenablage ist ein Systemdienst, der von der gesamten Windows-Sitzung gemeinsam verwendet werden, damit sie nicht über ein Handle oder einer eigenen Klasse verfügt. Sie verwalten die Zwischenablage über Memberfunktionen der Klasse [CWnd](../mfc/reference/cwnd-class.md).

## <a name="what-do-you-want-to-know-more-about"></a>Was möchten Sie mehr erfahren

- [Verwenden des jeweiligen zwischenablagemechanismus](../mfc/clipboard-when-to-use-each-clipboard-mechanism.md)

- [Mithilfe der herkömmlichen Windows-Zwischenablage-API](../mfc/clipboard-using-the-windows-clipboard.md)

- [Verwenden des OLE-zwischenablagemechanismus](../mfc/clipboard-using-the-ole-clipboard-mechanism.md)

- [Kopieren und Einfügen von Daten](../mfc/clipboard-copying-and-pasting-data.md)

- [Hinzufügen anderer Formate](../mfc/clipboard-adding-other-formats.md)

- [Die Windows-Zwischenablage](https://msdn.microsoft.com/library/ms648709)

- [Implementieren von Drag & Drop (OLE)](../mfc/drag-and-drop-ole.md)

## <a name="see-also"></a>Siehe auch

[Elemente der Benutzeroberfläche](../mfc/user-interface-elements-mfc.md)
