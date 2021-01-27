---
uid: Microsoft.Quantum.Diagnostics.EqualityFactCP
title: Equalityfaktcp-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactCP
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: a207ba1c4d08ec58095f5db34ee32c7341002920
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829169"
---
# <a name="equalityfactcp-function"></a>Equalityfaktcp-Funktion

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bestätigt, dass eine komplexe Zahl über den erwarteten Wert verfügt.

```qsharp
function EqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar, message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--complexpolar"></a>tatsächlich: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

Der zu überprüfende Wert.


### <a name="expected--complexpolar"></a>erwartet: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

Der erwartete Wert.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Fehlermeldungs Zeichenfolge, die verwendet wird, wenn die-Assertion ausgelöst wird



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

