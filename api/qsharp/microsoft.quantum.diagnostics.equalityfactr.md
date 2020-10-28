---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: Equalityfaktr-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 2b293dc581ed58f7e3864a952fb3ecafa68e759c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702654"
---
# <a name="equalityfactr-function"></a>Equalityfaktr-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


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

