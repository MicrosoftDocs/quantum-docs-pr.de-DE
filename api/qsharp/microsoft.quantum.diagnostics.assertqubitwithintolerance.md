---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Assertqubitwithintoleranz-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 7f57fc7a29d3eb86dc94cb24230d52b37eb6971d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853436"
---
# <a name="assertqubitwithintolerance-operation"></a>Assertqubitwithintoleranz-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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



## <a name="remarks"></a>Bemerkungen

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> ermöglicht das Assert von willkürlichen Qubit-Zuständen anstelle von $Z $ eigen Zuständen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertqubitisinstatewithintoleranz](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)