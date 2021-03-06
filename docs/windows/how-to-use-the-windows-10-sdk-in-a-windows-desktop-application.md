---
title: 'Gewusst wie: Verwenden des Windows 10-SDKs in einer Windows-Desktopanwendung'
ms.custom: get-started-article
ms.date: 07/12/2018
ms.assetid: eed6421e-9355-44a6-9582-3f1d453a6d44
ms.openlocfilehash: ed860a229866991b01266093058b71cc2ae84986
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50669117"
---
# <a name="how-to-use-the-windows-10-sdk-in-a-windows-desktop-application"></a>Gewusst wie: Verwenden des Windows 10-SDKs in einer Windows-Desktopanwendung

Wenn Sie ein klassisches Windows-desktop-Projekt in Visual Studio 2017 erstellen, ist es wird standardmäßig eingerichtet, mit der Version von Windows 10 SDK zu erstellen, die installiert wurde, wenn die C++-Desktop-Workload installiert oder zuletzt aktualisiert wurde. Diese Version des Windows SDK ist kompatibel, mit Windows 7 und höher. Finden Sie unter [verwenden der Windows-Header](/windows/desktop/WinProg/using-the-windows-headers) Informationen für bestimmte Versionen von Windows.

Wenn Sie eine frühere Version des SDK abzielen möchten, können Sie öffnen **Projekt | Eigenschaften** , und wählen Sie die anderen SDK-Versionen in der Dropdownliste für die Windows SDK-Version verfügbar.

Ab Visual Studio 2015 und Windows 10-SDKS, wurde die CRT-Bibliothek getrennt, in zwei Teile, eine (Bibliothek Ucrtbase), die Funktionen enthält, die in universellen Windows-Apps verwendet werden, und alles andere (vcruntime140) enthält. Da das Windows 10-SDK neue Funktionen enthält, z. B. zahlreiche C99-Funktionen, müssen Sie die folgenden Schritte ausführen, um diese Funktionen verwenden zu können. Siehe [CRT Library Features](../c-runtime-library/crt-library-features.md).

### <a name="to-target-the-windows-10-sdk"></a>Ausrichten auf das Windows 10-SDK

1. Stellen Sie sicher, dass das Windows 10-SDK installiert ist. Das Windows 10 SDK installiert ist, als Teil der **Desktopentwicklung mit C++** arbeitsauslastung. Eine eigenständige Version finden Sie unter [Downloads und tools für Windows 10](https://developer.microsoft.com/windows/downloads).

2. Öffnen Sie das Kontextmenü für den Projektknoten, und wählen Sie **SDK-Version neu zuweisen**aus.

   ![Neuzuweisen von SDK-Version](../windows/media/retargetingwindowssdk1.PNG "RetargetingWindowsSDK1")

   Das Dialogfeld **Projektmappenaktionen überprüfen** wird angezeigt.

   ![Lösungsaktionen](../windows/media/retargetingwindowssdk2.PNG "RetargetingWindowsSDK2")

3. In der **Zielplattformversion** Dropdown Liste, wählen Sie die Version des Windows 10 SDK ausgerichtet werden sollen. Klicken Sie auf „OK“, um die Änderung zu übernehmen.

   Beachten Sie, dass „8.1“ sich in diesem Zusammenhang auf die Version des Windows-SDKs bezieht, die ebenfalls abwärtskompatibel mit Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 und Windows Vista ist.

   Wenn Sie diesen Schritt erfolgreich durchgeführt haben, wird der folgende Text im Ausgabefenster angezeigt:

   `Retargeting End: 1 completed, 0 failed, 0 skipped`

4. Öffnen Sie die Projekteigenschaften, und achten Sie im Abschnitt **Konfigurationseigenschaften, Allgemein** auf die Werte für **Version der Windows-Zielplattform**. Wenn Sie den Wert hier ändern, hat dies die gleichen Auswirkungen wie dieses Verfahren. Siehe [General Property Page (Project)](../ide/general-property-page-project.md).

   ![Version der Zielplattform](../windows/media/retargetingwindowssdk3.PNG "RetargetingWindowsSDK3")

   Diese Aktion ändert die Werte der Projektmakros, die Pfade zu den Headerdateien und Bibliotheksdateien enthalten. Um herauszufinden, was geändert, in der **Visual C++-Verzeichnisse** im Abschnitt der **Projekteigenschaften** Dialogfeld Wählen Sie eine der Eigenschaften wie die **Includeverzeichnisse**, auswählen Öffnen der Dropdownliste aus, und wählen \<Bearbeiten >. Das Dialogfeld **Includeverzeichnisse** wird angezeigt.

   ![Dialogfeld für die Verzeichnisse enthalten](../windows/media/retargetingwindowssdk4.PNG "RetargetingWindowsSDK4")

   Wählen Sie die **Makros >>** Schaltfläche, und blättern Sie in der Liste der Makros, die Windows SDK-Makros, um alle neuen Werte anzuzeigen.

   ![Windows SDK-Makros](../windows/media/retargetingwindowssdk5.PNG "RetargetingWindowsSDK5")

5. Wiederholen Sie dies bei Bedarf für andere Projekte, und erstellen Sie die Projektmappe neu.

### <a name="to-target-the-windows-81-sdk"></a>Ausrichten auf das Windows 8.1-SDK

1. Öffnen Sie das Kontextmenü für den Projektknoten, und wählen Sie **SDK-Version neu zuweisen**aus.

2. In der **Zielplattformversion** Dropdownliste wählen **8.1**.

## <a name="see-also"></a>Siehe auch

[Windows-Desktopanwendungen (Visual C++)](../windows/how-to-use-the-windows-10-sdk-in-a-windows-desktop-application.md)