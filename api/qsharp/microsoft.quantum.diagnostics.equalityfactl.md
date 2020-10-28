---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: Equalityfaktl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: 5e590af581be4e41df9d2081260409c454e3be4b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702660"
---
# <a name="equalityfactl-function"></a>Equalityfaktl-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass eine klassische bigint-Variable über den erwarteten Wert verfügt.

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--bigint"></a>tatsächlicher Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Die Zahl, die geprüft werden soll.


### <a name="expected--bigint"></a>erwartet: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Der erwartete Wert.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Fehlermeldungs Zeichenfolge, die verwendet wird, wenn die-Assertion ausgelöst wird



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

