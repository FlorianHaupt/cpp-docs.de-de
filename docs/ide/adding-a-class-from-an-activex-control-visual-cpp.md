---
title: Hinzufügen einer Klasse aus einem ActiveX-Steuerelement (Visual C++)
ms.date: 09/07/2018
helpviewer_keywords:
- ActiveX controls [C++], adding classes
- classes [C++], creating
ms.assetid: 729fcb37-54b8-44d5-9b4e-50bb16e0eea4
ms.openlocfilehash: c78919aeee2d2577cd7371952d95c57c17b1e5ba
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50466624"
---
# <a name="adding-a-class-from-an-activex-control-visual-c"></a>Hinzufügen einer Klasse aus einem ActiveX-Steuerelement (Visual C++)

Verwenden Sie diesen Assistenten, um eine MFC-Klasse aus einer Schnittstelle in einem verfügbaren ActiveX-Steuerelement zu erstellen. Sie können eine MFC-Klasse in eine [MFC-Anwendung](../mfc/reference/creating-an-mfc-application.md), eine [MFC-DLL](../mfc/reference/creating-an-mfc-dll-project.md) oder ein [MFC-ActiveX-Steuerelement](../mfc/reference/creating-an-mfc-activex-control.md) einfügen.

> [!WARNING]
> Ab Version 15.9 von Visual Studio 2017 ist dieser Codeassistent veraltet. Er wird in einer zukünftigen Version von Visual Studio entfernt. Dieser Assistent wird nur selten verwendet. Die Entfernung dieses Assistenten wirkt sich nicht auf die allgemeine Unterstützung für Active Template Library (ATL) und Microsoft Foundation Classes (MFC) aus. In [dieser Umfrage](https://www.surveymonkey.com/r/QDWKKCN) können Sie Ihr Feedback zu dieser Veraltung mitteilen. Ihr Feedback ist uns wichtig.

> [!NOTE]
>  Sie müssen Ihr MFC-Projekt nicht mit aktiver Automatisierung erstellen, um eine Klasse aus einem ActiveX-Steuerelement hinzuzufügen.

Ein ActiveX-Steuerelement ist eine wiederverwendbare Softwarekomponente, die auf dem Component Object Model (COM) basiert. Dieses Modell unterstützt zahlreiche OLE-Funktionen und kann an die unterschiedlichsten Softwareanforderungen angepasst werden. ActiveX-Steuerelemente sind sowohl für den herkömmlichen Einsatz in ActiveX-Steuerelementcontainern als auch für die Verwendung in World Wide Web-Seiten im Internet geeignet.

### <a name="to-add-an-mfc-class-from-an-activex-control"></a>So fügen Sie eine MFC-Klasse aus einem ActiveX-Steuerelement hinzu

1. Klicken Sie entweder im **Projektmappen-Explorer** oder in der [Klassenansicht](/visualstudio/ide/viewing-the-structure-of-code) mit der rechten Maustaste auf den Namen des Projekts, dem Sie die ActiveX-Steuerelementklasse hinzufügen möchten.

1. Klicken Sie im Kontextmenü auf die Option **Hinzufügen**, und klicken Sie danach auf **Klasse hinzufügen**.

1. Klicken Sie im Dialogfeld [Klasse hinzufügen](../ide/add-class-dialog-box.md) im Bereich „Vorlagen“ auf **MFC-Klasse von ActiveX-Steuerelement**, und klicken Sie dann auf **Öffnen**, um den [Assistenten zum Hinzufügen einer ActiveX-Steuerelementklasse](../ide/add-class-from-activex-control-wizard.md) anzuzeigen.

Im Assistenten können Sie mehrere Schnittstellen in einem ActiveX-Steuerelement hinzufügen. Ebenso können Sie Klassen aus mehreren ActiveX-Steuerelementen in einer einzelnen Assistenten-Sitzung erstellen.

Sie können Klassen aus ActiveX-Steuerelementen hinzufügen, die im System registriert sind oder sich in Typbibliotheksdateien befinden (TLB-, OLB-, DLL-, OCX- oder EXE-Dateien), ohne diese zuerst im System registrieren zu müssen. Weitere Informationen zum Registrieren von ActiveX-Steuerelementen finden Sie unter [Registering OLE Controls (Registrieren von OLE-Steuerelementen)](../mfc/reference/registering-ole-controls.md).

Der Assistent erstellt für jede Schnittstelle, die Sie aus dem ausgewählten ActiveX-Steuerelement hinzufügen, eine MFC-Klasse, die von [CWnd](../mfc/reference/cwnd-class.md) oder [COleDispatchDriver](../mfc/reference/coledispatchdriver-class.md) abgeleitet wird.

## <a name="see-also"></a>Siehe auch

[MFC-ActiveX-Steuerelemente](../mfc/mfc-activex-controls.md)<br>
[Einführung in COM und ATL](../atl/introduction-to-com-and-atl.md)