---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: Equalityfaktr-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 86d2ddff79f0bca7badd95a2fe2156c558fa7f86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853327"
---
# <a name="equalityfactr-function"></a>Equalityfaktr-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bestätigt, dass eine klassische Ergebnisvariable über den erwarteten Wert verfügt.

```qsharp
function EqualityFactR (actual : Result, expected : Result, message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--__invalidresult__"></a>tatsächlicher Wert: __ungültig <Result>__

Die zu überprüfende Variable.


### <a name="expected--__invalidresult__"></a>erwartet: __ungültig <Result>__

Der erwartete Wert.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Fehlermeldungs Zeichenfolge, die verwendet wird, wenn die-Assertion ausgelöst wird



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

