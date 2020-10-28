---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Assertallzerowithintoleranz-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 5e401904086323fabef7914d34463f50e4c38862
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702785"
---
# <a name="assertallzerowithintolerance-operation"></a>Assertallzerowithintoleranz-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bestätigen Sie, dass die angegebenen Qubits alle in $ \ket {0} $ State bis zu einer gegebenen Toleranz aufweisen.

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit
```


## <a name="input"></a>Eingabe

### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits, die in $ \ket {0} $ State übergeben werden.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Die Genauigkeit, mit der sich der Status in "$ \ket $ State" befinden sollte. {0}



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertqubitwithintoleranz](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)