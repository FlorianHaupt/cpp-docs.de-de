---
title: Erstellen transparenter oder invertierter Bereiche in Gerätebildern (Bildbearbeitung für Symbole)
ms.date: 11/04/2016
helpviewer_keywords:
- cursors [C++], screen regions
- inverse colors [C++], device images
- transparent regions, device images
- transparency, device images
- Image editor [C++], device images
- inverse regions, device images
- cursors [C++], transparent regions
- screen colors
- regions, transparent
- icons [C++], transparent regions
- display devices [C++], transparent and screen regions
- transparent regions in devices
- regions, inverse
- colors [C++], Image editor
- device projects [C++], transparent images
- icons [C++], screen regions
ms.assetid: a994954b-b039-4391-a535-58d1fa10fc3b
ms.openlocfilehash: 3c4f5aa0b63259fbe42c353525e52319db1b0667
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50626641"
---
# <a name="creating-transparent-or-inverse-regions-in-device-images-image-editor-for-icons"></a>Erstellen transparenter oder invertierter Bereiche in Gerätebildern (Bildbearbeitung für Symbole)

In der [bildbearbeitung](../windows/image-editor-for-icons.md), das erste Symbol oder Cursor Abbild ein transparent Attribut aufweist. Obwohl das Symbol und der Cursor rechteckigen sind, werden viele nicht in dieser Form angezeigt, da Teile des Bilds transparent sind; der zugrunde liegenden Bildes auf dem Bildschirm zeigt durch das Symbol oder Cursor. Wenn Sie ein Symbol ziehen, möglicherweise Teile des Bilds in eine invertierte Farbe angezeigt. Sie erstellen diese Auswirkungen durch Festlegen der Bildschirmfarbe und invertierte Farbe in der [Fenster "Farben"](../windows/colors-window-image-editor-for-icons.md).

Die Bildschirm- und invertierte Farben, die Sie auf die Symbole anwenden und Cursor entweder Form und Farbe des abgeleiteten Bildes oder invertierter Bereiche bestimmt. Die Farben zeigen die Teile des Bilds, das diese Attribute besitzen. Sie können die Farben ändern, die die Attribute Fensterfarbe und Inverse Farbe im Bearbeitungsmodus darstellen. Diese Änderungen wirken sich nicht auf die Darstellung des Symbols oder Cursors in Ihrer Anwendung aus.

> [!NOTE]
> Je nach den aktiven Einstellungen oder der Version unterscheiden sich die Dialogfelder und Menübefehle auf Ihrem Bildschirm möglicherweise von den in der **Hilfe** beschriebenen. Klicken Sie im Menü **Extras** auf **Einstellungen importieren und exportieren** , um die Einstellungen zu ändern. Weitere Informationen finden Sie unter [Personalisieren von Visual Studio-IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).

### <a name="to-create-transparent-or-inverse-regions"></a>Erstellen transparenter oder invertierter Bereiche

1. In der **Farben** Fenster klicken Sie auf die **Fensterfarbe** Auswahl oder das **Inverse Farbe** Selektor.

2. Wenden Sie den Bildschirm oder eine invertierte Farbe auf Ihrem Image mithilfe eines Tools zeichnen. Weitere Informationen zum Zeichnen des Tools finden Sie unter [mithilfe eines Tools zeichnen](using-a-drawing-tool-image-editor-for-icons.md).

### <a name="to-change-the-screen-or-inverse-color"></a>So ändern Sie den Bildschirm oder Inverse Farbe

1. Wählen Sie entweder die **Fensterfarbe** Auswahl oder das **Inverse Farbe** Selektor.

2. Wählen Sie eine Farbe aus der **Farben** Palette in der **Farben** Fenster.

   Die Komplementärfarbe wird automatisch für die andere festgelegt.

   > [!TIP]
   > Doppelklicken auf die **Fensterfarbe** oder **Inverse Farbe** Auswahl der [benutzerdefinierte Farbauswahl (Dialogfeld)](../windows/custom-color-selector-dialog-box-image-editor-for-icons.md) angezeigt wird.

Informationen zum Hinzufügen von Ressourcen zu verwalteten Projekten finden Sie unter [Ressourcen in Desktop-Apps](/dotnet/framework/resources/index) in die *(.NET Framework Developer's Guide*. Weitere Informationen zum manuellen Hinzufügen von Ressourcendateien zu verwalteten Projekten, den Zugriff auf Ressourcen, zum Anzeigen statischer Ressourcen und Zuweisen von Ressourcenzeichenfolgen zu Eigenschaften, finden Sie unter [Erstellen von Ressourcendateien für Desktop-Apps](/dotnet/framework/resources/creating-resource-files-for-desktop-apps). Weitere Informationen zur Globalisierung und Lokalisierung von Ressourcen in verwalteten apps finden Sie unter [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index).

## <a name="requirements"></a>Anforderungen

Keiner

## <a name="see-also"></a>Siehe auch

[Zugriffstasten](../windows/accelerator-keys-image-editor-for-icons.md)<br/>
[Symbole und Cursor: Bildressourcen für Anzeigegeräte](../windows/icons-and-cursors-image-resources-for-display-devices-image-editor-for-icons.md)