---
title: ATL-Unterstützung für DHTML-Steuerelemente
ms.date: 11/04/2016
helpviewer_keywords:
- HTML controls, ATL support
- DHTML controls, ATL support
- DHTML controls
ms.assetid: 4ba98098-da5d-4362-96ad-8372f816c307
ms.openlocfilehash: 321c8c14f2049622b43741cfa9d856cb00e2cd61
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50638684"
---
# <a name="atl-support-for-dhtml-controls"></a>ATL-Unterstützung für DHTML-Steuerelemente

Verwendung von ATL, können Sie ein Steuerelement mit Dynamic HTML (DHTML)-Funktion erstellen. Ein ATL-DHTML-Steuerelement:

- Das WebBrowser-Steuerelement hostet.

- Gibt an, mit HTML, die Benutzeroberfläche (UI) des DHTML-Steuerelements.

- Greift auf das WebBrowser-Objekt und seine Methoden über die Schnittstelle, [IWebBrowser2](https://msdn.microsoft.com/library/aa752127.aspx).

- Verwaltet die Kommunikation zwischen C++-Code und HTML.

DHTML-Steuerelements entspricht keinem anderen ATL-Steuerelement, außer das DHTML-Steuerelement eine zusätzliche Dispatchschnittstelle enthält. Finden Sie unter der Abbildung im [Identifizieren von Elementen des DHTML-Steuerelementprojekts](../atl/identifying-the-elements-of-the-dhtml-control-project.md) eine Abbildung der zur Verfügung gestellt, in das Standardprojekt für die DHTML-Schnittstellen.

Sie können das ATL-DHTML-Steuerelement in einem Webbrowser oder andere Container, z. B. den Testcontainer für ActiveX-Steuerelemente anzeigen.

## <a name="in-this-section"></a>In diesem Abschnitt

[Identifizieren von Elementen des DHTML-Steuerelementprojekts](../atl/identifying-the-elements-of-the-dhtml-control-project.md)<br/>
Beschreibt die Elemente eines DHTML-Steuerelementprojekts.

[Aufrufen von C++-Code aus DHTML](../atl/calling-cpp-code-from-dhtml.md)<br/>
Stellt ein Beispiel für das Aufrufen von C++-Code aus DHTML-Steuerelements bereit.

[Erstellen eines ATL-DHTML-Steuerelements](../atl/creating-an-atl-dhtml-control.md)<br/>
Enthält die Schritte zum Erstellen eines DHTML-Steuerelements.

[Prüfen des ATL-DHTML-Steuerelements](../atl/testing-the-atl-dhtml-control.md)<br/>
Zeigt, wie zum Erstellen und testen die anfängliche DHTML-Steuerelementprojekts.

[Ändern des ATL-DHTML-Steuerelements](../atl/modifying-the-atl-dhtml-control.md)<br/>
Zeigt, wie einige Funktionen des Steuerelements hinzu.

[Prüfen des geänderten ATL-DHTML-Steuerelements](../atl/testing-the-modified-atl-dhtml-control.md)<br/>
Zeigt, wie zum Erstellen und testen die Funktionalität des Steuerelements hinzugefügt.

## <a name="related-sections"></a>Verwandte Abschnitte

[ATL](../atl/active-template-library-atl-concepts.md)<br/>
Enthält Links zu konzeptionellen Themen über die Programmierung mit der Active Template Library.

