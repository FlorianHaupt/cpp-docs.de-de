---
title: Bereitstellen einer Visual C++-Anwendung in einem lokalen Anwendungsordner
ms.date: 09/17/2018
helpviewer_keywords:
- deploying Visual C++ applications
ms.assetid: 47a81c47-9dbe-47c6-96cc-fbb2fda5e6ad
ms.openlocfilehash: 6715dacf6e00aacf3ba3ef7e6cd3773f48fd8e2f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50596910"
---
# <a name="walkthrough-deploying-a-visual-c-application-to-an-application-local-folder"></a>Exemplarische Vorgehensweise: Bereitstellen einer Visual C++-Anwendung in einem lokalen Anwendungsordner

In diesem Artikel wird beschrieben, wie eine Visual C++-Anwendung durch Kopieren von Dateien in den Ordner bereitgestellt wird.

## <a name="prerequisites"></a>Erforderliche Komponenten

- Einen Computer, auf dem Visual Studio installiert ist.

- Einen zusätzlichen Computer, auf dem keine Visual C++-Bibliotheken vorhanden sind.

### <a name="to-deploy-an-application-to-an-application-local-folder"></a>So stellen Sie eine Anwendung in einem lokalen Anwendungsordner bereit

1. Erstellen Sie eine MFC-Anwendung, indem Sie die folgenden Schritte unter [Exemplarische Vorgehensweise: Bereitstellen einer Visual C++-Anwendung mithilfe eines Setup-Projekts](walkthrough-deploying-a-visual-cpp-application-by-using-a-setup-project.md) befolgen.

1. Kopieren Sie die entsprechenden MFC- und CRT-Bibliotheksdateien (C Run-Time) aus dem Visual Studio-Installationsverzeichnis im Ordner \\VC\\redist\\*version*, und fügen Sie sie dann in den Ordner „\Release\“ Ihres MFC-Projekts ein. Weitere Informationen über andere Dateien, die Sie möglicherweise kopieren müssen, finden Sie unter [Determining Which DLLs to Redistribute (Ermitteln der zu verteilenden DLLs)](determining-which-dlls-to-redistribute.md).

1. Führen Sie die MFC-Anwendung auf einem zweiten Computer aus, der über keine der Visual C++-Bibliotheken verfügt.

   1. Kopieren Sie die Inhalte des Ordners „\Release\“, und fügen Sie sie in den Anwendungsordner auf dem zweiten Computer ein.

   1. Führen Sie die Anwendung auf dem zweiten Computer aus.

   Die Anwendung wird erfolgreich ausgeführt, da die Visual C++-Bibliotheken im lokalen Anwendungsordner verfügbar sind.

## <a name="see-also"></a>Siehe auch

[Bereitstellungsbeispiele](deployment-examples.md)<br/>
