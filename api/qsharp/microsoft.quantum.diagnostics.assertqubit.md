---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Assertqubit-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: 8fcdd8de9250348e1dd1173052b53be978f2a0c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853457"
---
# <a name="assertqubit-operation"></a>Assertqubit-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Bestätigt, dass sich das Qubit `q` im erwarteten eigen Zustand des Pauli Z-Operators befindet.

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="expected--__invalidresult__"></a>erwartet: __ungültig <Result>__

Der Zustand, in dem das Qubit erwartet wird: `Zero` oder `One` .


### <a name="q--qubit"></a>q: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, dessen Zustand bestätigt wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> ermöglicht das Assert von willkürlichen Qubit-Zuständen anstelle von $Z $ eigen Zuständen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertqubitisinstatewithintoleranz](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)