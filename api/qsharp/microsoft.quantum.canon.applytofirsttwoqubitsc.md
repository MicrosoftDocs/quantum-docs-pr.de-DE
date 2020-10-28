---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: Applydefirsttwoqubitsc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 97706ffcc8700a0055ff37bbbaccc6fb4f8854b6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704807"
---
# <a name="applytofirsttwoqubitsc-operation"></a>Applydefirsttwoqubitsc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Vorgang auf die ersten beiden Qubits im Register an.
Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="op--qubitqubit--unit-ctl"></a>OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Ein Vorgang, der auf die ersten beiden Qubits angewendet werden soll.


### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit-Array zu den ersten zwei Qubits, auf die der Vorgang angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Das entspricht:

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyjefirsttwoqubits](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)