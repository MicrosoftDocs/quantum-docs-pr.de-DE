---
uid: Microsoft.Quantum.Diagnostics.EqualityFactI
title: Equalityfakti-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactI
qsharp.summary: Asserts that a classical Int variable has the expected value.
ms.openlocfilehash: c41cb5548e8dfebb4d1c1a1c052306878c85e821
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853349"
---
# <a name="equalityfacti-function"></a>Equalityfakti-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bestätigt, dass eine klassische int-Variable über den erwarteten Wert verfügt.

```qsharp
function EqualityFactI (actual : Int, expected : Int, message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--int"></a>tatsächlicher Wert: [int](xref:microsoft.quantum.lang-ref.int)

Die Zahl, die geprüft werden soll.


### <a name="expected--int"></a>erwartet: [int](xref:microsoft.quantum.lang-ref.int)

Der erwartete Wert.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Fehlermeldungs Zeichenfolge, die verwendet wird, wenn die-Assertion ausgelöst wird



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

