---
title: ptr::operator bool
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ptr::operator bool
- ptr.operator bool
- operator bool
- msclr::com::ptr::operator bool
- msclr.com.ptr.operator bool
helpviewer_keywords:
- ptr::operator bool
ms.assetid: 31123377-6ecd-4cef-9b75-3db3996fbcd1
ms.openlocfilehash: 185db15a62cc676c771f60a54c583e19e28e95be
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50509668"
---
# <a name="ptroperator-bool"></a>ptr::operator bool

Operator für die Verwendung von `com::ptr` in einem bedingten Ausdruck.

## <a name="syntax"></a>Syntax

```
operator bool();
```

## <a name="return-value"></a>Rückgabewert

**"true"** Wenn das COM-Objekt im Besitz des Benutzers gültig ist. **"false"** andernfalls.

## <a name="remarks"></a>Hinweise

Das COM-Objekt im Besitz des Benutzers ist gültig, wenn er nicht ist `nullptr`.

Dieser Operator konvertiert tatsächlich in `_detail_class::_safe_bool` ist sicherer als `bool` , da es in einen ganzzahligen Typ konvertiert werden kann.

## <a name="example"></a>Beispiel

In diesem Beispiel implementiert eine CLR-Klasse, verwendet eine `com::ptr` , umschließen die privaten Member `IXMLDOMDocument` Objekt. Die `CreateInstance` Memberfunktion verwendet `operator bool` nach dem Erstellen der neuen Document-Objekt, um zu bestimmen, ob es gültig ist und in die Konsole geschrieben werden, wenn es sich handelt.

```
// comptr_op_bool.cpp
// compile with: /clr /link msxml2.lib
#include <msxml2.h>
#include <msclr\com\ptr.h>

#import <msxml3.dll> raw_interfaces_only

using namespace System;
using namespace System::Runtime::InteropServices;
using namespace msclr;

// a ref class that uses a com::ptr to contain an
// IXMLDOMDocument object
ref class XmlDocument {
public:
   void CreateInstance(String^ progid) {
      if (!m_ptrDoc) {
         m_ptrDoc.CreateInstance(progid);
         if (m_ptrDoc) { // uses operator bool
            Console::WriteLine("DOM Document created.");
         }
      }
   }

   // note that the destructor will call the com::ptr destructor
   // and automatically release the reference to the COM object

private:
   com::ptr<IXMLDOMDocument> m_ptrDoc;
};

// use the ref class to handle an XML DOM Document object
int main() {
   try {
      XmlDocument doc;
      // create the instance from a progid string
      doc.CreateInstance("Msxml2.DOMDocument.3.0");
   }
   catch (Exception^ e) {
      Console::WriteLine(e);
   }
}
```

```Output
DOM Document created.
```

## <a name="requirements"></a>Anforderungen

**Headerdatei** \<msclr\com\ptr.h >

**Namespace** msclr::com

## <a name="see-also"></a>Siehe auch

[ptr-Member](../dotnet/ptr-members.md)<br/>
[ptr::operator!](../dotnet/ptr-operator-logical-not.md)