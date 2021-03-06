---
title: Erstellen einer MFC-Anwendung im Webbrowserstil
ms.date: 06/25/2018
f1_keywords:
- vc.appwiz.mfcweb.project
helpviewer_keywords:
- MFC, Web applications
- Web browsers, creating from MFC architecture
- Web browsers
- Web applications [MFC], creating
ms.assetid: 257f8c03-33c3-428c-832e-0b70aff6168d
ms.openlocfilehash: 1fd61b3e6bcb2f429c43edcabb41e166bcec95c6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50466156"
---
# <a name="creating-a-web-browser-style-mfc-application"></a>Erstellen einer MFC-Anwendung im Webbrowserstil

Eine Web-Anwendung im Webbrowserstil kann Informationen aus dem Internet (z. B. HTML- oder aktive Dokumente) oder einem Intranet als auch Ordner im lokalen Dateisystem und in einem Netzwerk zugreifen. Durch Ableiten von der Anwendung Ansichtsklasse aus [CHtmlView](../../mfc/reference/chtmlview-class.md)effektiv Sie machen der Anwendung einen Webbrowser, indem Sie die Ansicht das WebBrowser-Steuerelements bereitstellt.

### <a name="to-create-a-web-browser-application-based-on-the-mfc-documentview-architecture"></a>Zum Erstellen einer Web-Browser-Anwendung basierend auf der MFC Dokument-/Ansichtarchitektur

1. Befolgen Sie die Anweisungen [Erstellen einer MFC-Anwendung](../../mfc/reference/creating-an-mfc-application.md).

1. Im MFC-Anwendungs-Assistenten [Anwendungstyp](../../mfc/reference/application-type-mfc-application-wizard.md) Seite stellen Sie sicher, dass die **Dokument-/Ansichtarchitektur** aktiviert ist. (Sie können wählen, ob **einzelnes Dokument** oder **mehrere Dokumente**, aber nicht **auf Dialogfeldern basierend**.)

1. Auf der [erstellte Klassen überprüfen](../../mfc/reference/generated-classes-mfc-application-wizard.md) verwenden Sie die **Basisklasse** Dropdown-Menü auswählen `CHtmlView`.

1. Wählen Sie alle anderen gewünschten Optionen in die skelettanwendung integriert.

1. Klicken Sie auf **Fertig stellen**.

Das WebBrowser-Steuerelement unterstützt das Webbrowsen über die Links und Navigation der Uniform Resource Locator (URL). Das Steuerelement unterhält eine Verlaufsliste, die dem Benutzer ermöglicht, Vorwärts navigieren und rückwärts durch vorher besucht haben Websites, Ordner und Dokumente. Das Steuerelement verwaltet direkt, die Navigation, Hyperlinks, Verlaufslisten, Favoriten und Sicherheit. Anwendungen können das WebBrowser-Steuerelement als eine active Document-Container zum Host sowie für aktive Dokumente verwenden. Daher können direkt in das WebBrowser-Steuerelement formatierungsmöglichkeiten Dokumente wie z. B. Microsoft Excel-Tabellen oder Word-Dokumente geöffnet und bearbeitet werden. Das WebBrowser-Steuerelement ist auch ein ActiveX-Steuerelementcontainer, der alle ActiveX-Steuerelement hosten können.

> [!NOTE]
>  Der WebBrowser ActiveX-Steuerelement (und somit auch `CHtmlView`) steht nur für Anwendungen, die unter Windows-Versionen, in denen Internet Explorer 4.0 oder höher installiert wurde.

Da `CHtmlView` implementiert einfach das Microsoft-Web-Browser-Steuerelement, die Unterstützung für das Drucken ist nicht wie andere [CView](../../mfc/reference/cview-class.md)-abgeleiteten Klassen. Stattdessen implementiert das WebBrowser-Steuerelement an die Benutzeroberfläche des Druckers und den Druckvorgang. Daher `CHtmlView` wird nicht unterstützt, Seitenansicht, und das Framework bietet keine andere drucken Supportfunktionen: z. B. [CView::OnPreparePrinting](../../mfc/reference/cview-class.md#onprepareprinting), [CView::OnBeginPrinting](../../mfc/reference/cview-class.md#onbeginprinting), und [CView::OnEndPrinting](../../mfc/reference/cview-class.md#onendprinting), die in anderen MFC-Anwendungen verfügbar sind.

`CHtmlView` fungiert als Wrapper für das Webbrowser-Steuerelement, wodurch Ihre Anwendung eine Ansicht auf einer Web- oder eine HTML-Seite. Der Assistent erstellt eine Außerkraftsetzung für die [OnInitialUpdate](../../mfc/reference/cview-class.md#oninitialupdate) -Funktion in der Ansichtsklasse, sodass ein Link zur Microsoft Visual C++-Website:

```cpp
void CWebView::OnInitialUpdate()
{
    CHtmlView::OnInitialUpdate();

    // TODO: This code navigates to a popular spot on the web.
    // Change the code to go where you'd like.
    Navigate2(_T("http://www.msdn.microsoft.com/vstudio/"),
        NULL,
        NULL);
}
```

Sie können diese Website durch ein eigenes ersetzen oder können Sie die [LoadFromResource](../../mfc/reference/chtmlview-class.md#loadfromresource) Memberfunktion versucht, eine HTML-Seite zu öffnen, die als den standardmäßigen Inhalt der Ansicht des Projekts Ressourcenskript befindet. Zum Beispiel:

```cpp
void CWebView::OnInitialUpdate()
{
    CHtmlView::OnInitialUpdate();

    // TODO: This code navigates to a popular spot on the web.
    // Change the code to go where you'd like.
    LoadFromResource(IDR_HTML1);
}
```

## <a name="see-also"></a>Siehe auch

[MFC-Beispiel-MFCIE](https://github.com/Microsoft/VCSamples)<br/>
[MFC-Anwendungs-Assistent](../../mfc/reference/mfc-application-wizard.md)<br/>
[Arbeiten mit Projekteigenschaften](../../ide/working-with-project-properties.md)<br/>
[Eigenschaftenseiten](../../ide/property-pages-visual-cpp.md)<br/>
[Arbeiten mit Projekteigenschaften](../../ide/working-with-project-properties.md)

