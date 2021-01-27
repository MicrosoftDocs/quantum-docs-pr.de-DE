---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Applypermutationusingdecompositionwithvariableorder-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: f33d2980ff1775b1ae8d2e2e7a4fa1e5cbe7d5ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858880"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a>Applypermutationusingdecompositionwithvariableorder-Vorgang

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Pertrauert die Verstärkung in einem Quantum-Zustand, wenn eine permutations mithilfe der Zerlegungs basierten Synthese verwendet wird.

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschreibung

Bei diesem Vorgang handelt es sich um eine allgemeinere Version von @"microsoft.quantum.synthesis.applypermutationusingdecomposition" , in der die Reihenfolge der Variablen angegeben werden kann. Eine andere Variablen Reihenfolge ändert die Zerlegungs Sequenz und die Wahrheitstabellen, die für die kontrollierten Gates verwendet werden @"microsoft.quantum.intrinsic.x" .  Wenn Sie die Reihenfolge der Variablen ändern, wird daher die Gesamtzahl der Gates geändert, die zur Umsetzung der Permutation verwendet werden.

## <a name="input"></a>Eingabe

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]

Eine permutations von $2 ^ n $ Elementen, beginnend bei 0.


### <a name="variableorder--int"></a>variableorder: [int](xref:microsoft.quantum.lang-ref.int)[]

Eine permutations von $n $-Elementen, beginnend bei 0.


### <a name="qubits--littleendian"></a>Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Eine Liste von $n $ Qubits, auf die die permutations angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Beispiel

So können Sie einen `SWAP` Vorgang synthetisieren:

```qsharp
using (qubits = Qubit[2]) {
  ApplyPermutationUsingDecompositionWithVariableOrder([0, 2, 1, 3], [1, 0], LittleEndian(qubits));
}
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Synthese. applypermutationusingzerlegung](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [Microsoft. Quantum. Synthese. applypermutationusingtransformation](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)