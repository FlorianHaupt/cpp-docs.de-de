---
title: /Zl (Kein Standardbibliotheksname)
ms.date: 11/04/2016
f1_keywords:
- /zi
- VC.Project.VCCLCompilerTool.OmitDefaultLibName
helpviewer_keywords:
- -Zl compiler option [C++]
- ZI compiler option
- Omit Default Library Name compiler option
- /Zl compiler option [C++]
- default libraries, omitting names
ms.assetid: b27d39d0-44d6-498c-84ae-27c1326fee59
ms.openlocfilehash: ba30efd76e94749dd261f3528535d674b5e155e9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50621909"
---
# <a name="zl-omit-default-library-name"></a>/Zl (Kein Standardbibliotheksname)

Lässt C Runtime Library Standardname aus der OBJ-Datei an. Standardmäßig legt der Compiler den Namen der Bibliothek in der OBJ-Datei ab, um den Linker zur richtigen Bibliothek zu leiten.

## <a name="syntax"></a>Syntax

```
/Zl
```

## <a name="remarks"></a>Hinweise

Weitere Informationen über die Standardbibliothek finden Sie unter [Use Run-Time Library](../../build/reference/md-mt-ld-use-run-time-library.md).

Sie können **/Zl** um OBJ-Dateien zu kompilieren, in eine Bibliothek eingefügt werden sollen. Obwohl nur eine kleine Menge an Speicherplatz für eine einzelne OBJ-Datei weglassen von Namen der Bibliothek gespeichert werden, spielt der gesamte Speicherplatz gespeichert in einer Bibliothek, die viele Objektmodule enthält.

Diese Option ist eine erweiterte Option. Das Festlegen dieser Option werden bestimmte C-Laufzeit-Bibliothek-Unterstützung, die möglicherweise, durch die Anwendung erforderlich, was zu Link-Time-Fehlern, wenn Ihre Anwendung, diese Unterstützung abhängt entfernt. Wenn Sie diese Option verwenden, müssen Sie die erforderlichen Komponenten auf andere Weise bereitstellen.

Verwendung [/NODEFAULTLIB (Bibliotheken ignorieren)](../../build/reference/nodefaultlib-ignore-libraries.md). Leiten Sie den Linker Bibliotheksverweise in allen OBJ-Dateien ignoriert werden sollen.

Weitere Informationen finden Sie unter [CRT Library Features (CRT-Bibliotheksfunktionen)](../../c-runtime-library/crt-library-features.md).

Beim Kompilieren mit **/Zl**, `_VC_NODEFAULTLIB` definiert ist.  Zum Beispiel:

```
// vc_nodefaultlib.cpp
// compile with: /Zl
void Test() {
   #ifdef _VC_NODEFAULTLIB
      int i;
   #endif

   int i;   // C2086
}
```

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Compileroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Ausführliche Informationen finden Sie unter [Working with Project Properties (Arbeiten mit Projekteigenschaften)](../../ide/working-with-project-properties.md).

1. Klicken Sie auf den Ordner **C/C++** .

1. Klicken Sie auf die **erweitert** Eigenschaftenseite.

1. Ändern der **Standardbibliotheknamen** Eigenschaft.

### <a name="to-set-this-compiler-option-programmatically"></a>So legen Sie diese Compileroption programmgesteuert fest

- Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.OmitDefaultLibName%2A>.

## <a name="see-also"></a>Siehe auch

[Compileroptionen](../../build/reference/compiler-options.md)<br/>
[Festlegen von Compileroptionen](../../build/reference/setting-compiler-options.md)