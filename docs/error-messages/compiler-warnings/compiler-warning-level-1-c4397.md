---
title: Compilerwarnung (Stufe 1) C4397
ms.date: 11/04/2016
f1_keywords:
- C4397
helpviewer_keywords:
- C4397
ms.assetid: 6346fdc2-dbbf-4fba-803a-32b0d0a707be
ms.openlocfilehash: 4ad690d78c1544adbe365a35ba3b5921c883631e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50498769"
---
# <a name="compiler-warning-level-1-c4397"></a>Compilerwarnung (Stufe 1) C4397

DefaultCharSetAttribute wird ignoriert.

<xref:System.Runtime.InteropServices.DefaultCharSetAttribute> wird von Visual C++-Compiler ignoriert. Um einen Zeichensatz für die DLL anzugeben, verwenden Sie die Option "Zeichensatz" von DllImport. Weitere Informationen finden Sie unter [mithilfe C++-Interop (implizites PInvoke)](../../dotnet/using-cpp-interop-implicit-pinvoke.md).

## <a name="example"></a>Beispiel

Im folgende Beispiel wird C4397 generiert.

```
// C4397.cpp
// compile with: /W1 /c /clr
using namespace System;
using namespace System::Runtime::InteropServices;

[module:DefaultCharSetAttribute(CharSet::Unicode)];   // C4397

[DllImport("kernel32", EntryPoint="CloseHandle", CharSet=CharSet::Unicode)]   // OK
extern "C" bool ImportDefault(IntPtr hObject);

public ref class MySettingVC {
public:
   void method() {
      ImportDefault(IntPtr::Zero);
   }
};

[StructLayout(LayoutKind::Explicit)]
public ref struct StructDefault1{};

public ref class ClassDefault1{};
```