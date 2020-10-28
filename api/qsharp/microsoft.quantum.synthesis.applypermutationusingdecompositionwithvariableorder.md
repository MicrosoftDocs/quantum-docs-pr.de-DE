---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Applypermutationusingdecompositionwithvariableorder-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 1edbc0a2948fdf3ae67f14b3c552676feaa7f498
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725299"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a>Applypermutationusingdecompositionwithvariableorder-Vorgang

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paketen [](https://nuget.org/packages/)


Pertrauert die Verstärkung in einem Quantum-Zustand, wenn eine permutations mithilfe der Zerlegungs basierten Synthese verwendet wird.

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei diesem Vorgang handelt es sich um eine allgemeinere Version von @"microsoft.quantum.synthesis.applypermutationusingdecomposition" , in der die Reihenfolge der Variablen angegeben werden kann. Eine andere Variablen Reihenfolge ändert die Zerlegungs Sequenz und die Wahrheitstabellen, die für die kontrollierten Gates verwendet werden @"microsoft.quantum.intrinsic.x" .  Wenn Sie die Reihenfolge der Variablen ändern, wird daher die Gesamtzahl der Gates geändert, die zur Umsetzung der Permutation verwendet werden.

## <a name="input"></a>Eingabe

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]

Eine permutations von $2 ^ n $ Elementen, beginnend bei 0.


### <a name="variableorder--int"></a>variableorder: [int](xref:microsoft.quantum.lang-ref.int)[]

Eine permutations von $n $-Elementen, beginnend bei 0.


### <a name="qubits--littleendian"></a>Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Eine Liste von $n $ Qubits, auf die die permutations angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Synthese. applypermutationusingzerlegung](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [Microsoft. Quantum. Synthese. applypermutationusingtransformation](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)