---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Assertallzerowithintoleranz-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 281855ec79d280c903ebb4d05614081767840778
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830857"
---
# <a name="assertallzerowithintolerance-operation"></a>Assertallzerowithintoleranz-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Bestätigen Sie, dass die angegebenen Qubits alle in $ \ket {0} $ State bis zu einer gegebenen Toleranz aufweisen.

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits, die in $ \ket {0} $ State übergeben werden.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Die Genauigkeit, mit der sich der Status in "$ \ket $ State" befinden sollte. {0}



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertqubitwithintoleranz](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)