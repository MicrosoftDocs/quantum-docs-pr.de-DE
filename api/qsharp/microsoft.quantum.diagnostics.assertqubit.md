---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Assertqubit-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: fa1f52da5a011cd914a0fda69b78cf5a4fd71e16
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702743"
---
# <a name="assertqubit-operation"></a>Assertqubit-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


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



## <a name="remarks"></a>Hinweise

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> ermöglicht das Assert von willkürlichen Qubit-Zuständen anstelle von $Z $ eigen Zuständen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertqubitisinstatewithintoleranz](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)