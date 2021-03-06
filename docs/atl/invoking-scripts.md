---
title: Aufrufen von Skripts (ATL)
ms.date: 11/04/2016
f1_keywords:
- StringRegister
helpviewer_keywords:
- StringRegister method
- scripts, invoking registry in ATL
ms.assetid: eabd41ee-586b-4266-9e92-5aaad04b73a4
ms.openlocfilehash: 170eb4c29571fcec8797727f54630894c9198442
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50650553"
---
# <a name="invoking-scripts"></a>Aufrufen von Skripts

[Verwenden von ersetzbaren Parametern (der Registrierungspräprozessor)](../atl/using-replaceable-parameters-the-registrar-s-preprocessor.md) wird erläutert, Ersatz-Zuordnungen und wird von der Registrierungsstelle Methode **AddReplacement**. Die Registrierungsstelle hat acht andere spezifische Methoden des Skripts, und alle werden in der folgenden Tabelle beschrieben.

|Methode|Syntaxbeschreibung /|
|------------|-------------------------|
|**ResourceRegister**|**HRESULT ResourceRegister (LPCOLESTR***ResFileName* **, "uint"** `nID` **, LPCOLESTR** `szType` **);**<br /><br /> Registriert das Skript in der Ressource eines Moduls enthalten. *ResFileName* gibt den UNC-Pfad für das Modul selbst. *nID* und *SzType* enthalten bzw. die ID und den Typ der Ressource.|
|**ResourceUnregister**|**HRESULT ResourceUnregister (LPCOLESTR***ResFileName* **, "uint"** `nID` **, LPCOLESTR** `szType` **);**<br /><br /> Hebt die Registrierung des Skripts, die in der Ressource eines Moduls enthalten. *ResFileName* gibt den UNC-Pfad für das Modul selbst. *nID* und *SzType* enthalten bzw. die ID und den Typ der Ressource.|
|**ResourceRegisterSz**|**HRESULT ResourceRegisterSz (LPCOLESTR***ResFileName* **, LPCOLESTR***SzID* **, LPCOLESTR** `szType` **);**<br /><br /> Registriert das Skript in der Ressource eines Moduls enthalten. *ResFileName* gibt den UNC-Pfad für das Modul selbst. *SzID* und *SzType* enthalten bzw. Zeichenfolgenbezeichner und den Typ der Ressource.|
|**ResourceUnregisterSz**|**HRESULT ResourceUnregisterSz (LPCOLESTR***ResFileName* **, LPCOLESTR***SzID* **, LPCOLESTR** `szType` **);**<br /><br /> Hebt die Registrierung des Skripts, die in der Ressource eines Moduls enthalten. *ResFileName* gibt den UNC-Pfad für das Modul selbst. *SzID* und *SzType* enthalten bzw. Zeichenfolgenbezeichner und den Typ der Ressource.|
|**FileRegister**|**HRESULT FileRegister (LPCOLESTR***FileName***);**<br /><br /> Registriert das Skript in einer Datei an. *FileName* ist ein UNC-Pfad zu einer Datei, die ein Ressourcenskript enthält (oder ist).|
|**FileUnregister**|**HRESULT FileUnregister (LPCOLESTR***FileName***);**<br /><br /> Hebt die Registrierung des Skripts in einer Datei. *FileName* ist ein UNC-Pfad zu einer Datei, die ein Ressourcenskript enthält (oder ist).|
|**StringRegister**|**HRESULT StringRegister (LPCOLESTR***Daten***);**<br /><br /> Registriert das Skript in einer Zeichenfolge. *Daten* enthält das Skript selbst.|
|**StringUnregister**|**HRESULT StringUnregister (LPCOLESTR***Daten***);**<br /><br /> Hebt die Registrierung des Skripts in einer Zeichenfolge. *Daten* enthält das Skript selbst.|

**ResourceRegisterSz** und **ResourceUnregisterSz**, ähneln **ResourceRegister** und **ResourceUnregister**, doch gestatten Ihnen eine Zeichenfolge angeben Bezeichner.

Die Methoden **FileRegister** und **FileUnregister** sind nützlich, wenn Sie nicht, dass das Skript in einer Ressource möchten oder das Skript in einer eigenen Datei werden soll. Die Methoden **StringRegister** und **StringUnregister** RGS-Datei in einem dynamisch zugewiesenen Zeichenfolge gespeichert werden können.

## <a name="see-also"></a>Siehe auch

[Erstellen von Registrierungsskripts](../atl/creating-registrar-scripts.md)

