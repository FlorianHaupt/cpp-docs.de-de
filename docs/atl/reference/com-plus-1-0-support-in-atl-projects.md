---
title: COM+ 1.0-Unterstützung in ATL-Projekte
ms.date: 11/04/2016
f1_keywords:
- vc.appwiz.ATL.MTS
helpviewer_keywords:
- ATL projects, COM+ 1.0 support
ms.assetid: 51fb08ac-d632-4657-a4e0-d3f989f0b6f8
ms.openlocfilehash: 4bc7683d6121dec748e30c1ea717042b9cf1ecbc
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50562460"
---
# <a name="com-10-support-in-atl-projects"></a>COM+ 1.0-Unterstützung in ATL-Projekte

Sie können die [ATL-Projektassistenten](../../atl/reference/creating-an-atl-project.md) zum Erstellen eines Projekts mit basic-Support für COM+ 1.0-Komponenten.

COM+ 1.0 wurde entwickelt, für die Entwicklung von verteilten Anwendungen mit Komponenten basiert. Darüber hinaus eine Laufzeitinfrastruktur für die Bereitstellung und Verwaltung der einzelnen Programme.

Bei Auswahl der **COM+ 1.0-Unterstützung** Kontrollkästchen, die der Assistent ändert das Buildskript im Linkschritt. Insbesondere die COM+ 1.0-Projekt enthält Links zu den folgenden Bibliotheken:

- comsvcs.lib hinzu:

- Mtxguid.lib

Bei Auswahl der **COM+ 1.0-Unterstützung** , Sie können auch Kontrollkästchen **Unterstützung Komponente Registrierungsstelle**. Die Registrierung der Komponente können Ihre COM+ 1.0-Objekt, rufen Sie eine Liste der Komponenten, Komponenten zu registrieren oder Aufheben der Registrierung Komponenten (einzeln oder alle auf einmal).

## <a name="see-also"></a>Siehe auch

[Grundlagen von ARL COM-Objekten](../../atl/fundamentals-of-atl-com-objects.md)<br/>
[Programmieren mit ATL- und C-Laufzeitcode](../../atl/programming-with-atl-and-c-run-time-code.md)<br/>
[Standardmäßige ATL-Projektkonfigurationen](../../atl/reference/default-atl-project-configurations.md)

