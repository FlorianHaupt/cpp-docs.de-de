---
title: ptr::~ptr
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- msclr.com.ptr.~ptr
- ptr.~ptr
- msclr::com.ptr::~ptr
- ~ptr
- ptr::~ptr
helpviewer_keywords:
- ptr::~ptr
ms.assetid: 5f644aa5-fe66-4992-a5f8-13ec1292c949
ms.openlocfilehash: 452876fb2b377048b3916e61d39467e2279cd4ad
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50618063"
---
# <a name="ptrptr"></a>ptr::~ptr

Destructs eine `com::ptr`.

## <a name="syntax"></a>Syntax

```
~ptr();
```

## <a name="remarks"></a>Hinweise

Der Zerstörung der `com::ptr` gibt alle Verweise, die es, auf die COM-Objekt besitzt frei. Vorausgesetzt, es keine weiteren Verweise frei, die auf die COM-Objekt sind, das COM-Objekt gelöscht werden, und dessen Speicher freigegeben.

## <a name="example"></a>Beispiel

In diesem Beispiel implementiert eine CLR-Klasse, verwendet eine `com::ptr` , umschließen die privaten Member `IXMLDOMDocument` Objekt.  In der `main` -Funktion, die beiden `XmlDocument` Destruktor des Objekts werden aufgerufen, wenn sie den Geltungsbereich verlässt die `try` blockieren, was in der zugrunde liegenden `com::ptr` Destruktor aufgerufen wird, Freigabe alle im Besitz des Benutzers Verweise auf COM -Objekt.

```
// comptr_dtor.cpp
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
   // construct the internal com::ptr with a null interface
   // and use CreateInstance to fill it
   XmlDocument(String^ progid) {
      m_ptrDoc.CreateInstance(progid);
   }

   // construct the internal com::ptr with a COM object
   XmlDocument(IXMLDOMDocument* pDoc) : m_ptrDoc(pDoc) {}

   // note that the destructor will call the com::ptr destructor
   // and automatically release the reference to the COM object

private:
   com::ptr<IXMLDOMDocument> m_ptrDoc;
};

// use the ref class to handle an XML DOM Document object
int main() {
   IXMLDOMDocument* pDoc = NULL;

   try {
      // create an XML DOM document object
      Marshal::ThrowExceptionForHR(CoCreateInstance(CLSID_DOMDocument30, NULL,
         CLSCTX_ALL, IID_IXMLDOMDocument, (void**)&pDoc));
      // construct the ref class with the COM object
      XmlDocument doc1(pDoc);

      // or create the class from a progid string
      XmlDocument doc2("Msxml2.DOMDocument.3.0");
   }
   // doc1 and doc2 destructors are called when they go out of scope
   // and the internal com::ptr releases its reference to the COM object
   catch (Exception^ e) {
      Console::WriteLine(e);
   }
   finally {
      if (NULL != pDoc) {
         pDoc->Release();
      }
   }
}
```

## <a name="requirements"></a>Anforderungen

**Headerdatei** \<msclr\com\ptr.h >

**Namespace** msclr::com

## <a name="see-also"></a>Siehe auch

[ptr-Member](../dotnet/ptr-members.md)<br/>
[ptr::ptr](../dotnet/ptr-ptr.md)<br/>
[ptr::CreateInstance](../dotnet/ptr-createinstance.md)