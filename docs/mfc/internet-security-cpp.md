---
title: Internetsicherheit (C++)
ms.date: 11/04/2016
helpviewer_keywords:
- code signing [MFC], Internet security
- sandboxing [MFC]
- digital signatures [MFC], Internet security
- code signing [MFC]
- Web application security [MFC]
- code access security [MFC], Internet security considerations
- security [MFC]
- security [MFC], Internet
- Internet applications [MFC], security
- Web application security [MFC], Internet security approaches
ms.assetid: bf0da697-81bc-41f0-83fa-d7f82ed83df8
ms.openlocfilehash: e7892793a82f2b030a99465a712e33e1b9ef4673
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50486098"
---
# <a name="internet-security-c"></a>Internetsicherheit (C++)

Code-Sicherheit ist ein großes Problem für Entwickler und für Benutzer von Internet-Anwendungen. Risiken bestehen: bösartiger Code, Code, die manipuliert wurden und Code von unbekannten Standorten oder Autoren.

Es gibt zwei grundlegende Ansätze zur Sicherheit bei der Entwicklung für das Internet. Der erste heißt "Sandboxing". Bei diesem Ansatz ist eine Anwendung auf einen bestimmten Satz von APIs beschränkt, und potenziell gefährlich sind z. B. Datei-e/a, in denen ein Programm Daten auf dem Computer eines Benutzers zerstören könnten, ausgeschlossen. Die zweite wird mithilfe von digitalen Signaturen implementiert. Dieser Ansatz ist für das Internet als "Shrinkwrap" bezeichnet. Code wird überprüft und mithilfe von privaten und öffentlichen Schlüsseln signiert. Bevor der Code ausgeführt wird, wird die digitale Signatur überprüft, stellen Sie sicher, dass der Code von einer bekannten, authentifizierten Quelle und der Code nicht geändert wurden, seit es signiert wurde.

Im ersten Fall verlassen Sie sich, dass die Anwendung wird nicht Schaden, und Sie den Ursprung der Anwendung vertrauen. Im zweiten Fall sind digitale Signaturen verwendet, um die Echtheit. Digitale Signatur ist ein Industriestandard zum Identifizieren, und geben Sie Details über den Herausgeber des Codes verwendet. Diese Technologien basieren auf Standards wie RSA und x. 509. Browser können in der Regel Benutzer wählen, wenn sie möchten zum Herunterladen und Ausführen von Code mit Unbekannter Herkunft.

## <a name="see-also"></a>Siehe auch

[MFC-Internetprogrammierungsaufgaben](../mfc/mfc-internet-programming-tasks.md)<br/>
[Grundlagen der MFC-Internetprogrammierung](../mfc/mfc-internet-programming-basics.md)

