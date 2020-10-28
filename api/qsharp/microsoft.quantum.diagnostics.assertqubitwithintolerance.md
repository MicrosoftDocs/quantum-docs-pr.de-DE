---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Assertqubitwithintoleranz-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 3fe4aa739c5e15199401aecb76ef551e52f6dcff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702714"
---
# <a name="assertqubitwithintolerance-operation"></a>Assertqubitwithintoleranz-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass das Qubit den `q` erwarteten Zustand des Pauli Z-Operators bis zu einer gegebenen Toleranz aufweist.

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>Eingabe

### <a name="expected--__invalidresult__"></a>erwartet: __ungültig <Result>__

Der Zustand, in dem das Qubit erwartet wird: `Zero` oder `One` .


### <a name="q--qubit"></a>q: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, dessen Zustand bestätigt wird.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Toleranz für die Wahrscheinlichkeit einer Messung des Qubit, das das erwartete Ergebnis zurückgibt.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> ermöglicht das Assert von willkürlichen Qubit-Zuständen anstelle von $Z $ eigen Zuständen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertqubitisinstatewithintoleranz](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)