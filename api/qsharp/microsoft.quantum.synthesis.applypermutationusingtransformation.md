---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: Applypermutationusingtransformation-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: a05b433eae2612bbf5c87522c4ef251976184aa8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192059"
---
# <a name="applypermutationusingtransformation-operation"></a>Applypermutationusingtransformation-Vorgang

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Pertrauert die Verstärkung in einem Quantum-Zustand, wenn eine permutations mithilfe der Transformations basierten Synthese verwendet wird.

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Diese Prozedur implementiert den unidirektionalen Transformations basierten Synthese Ansatz.  Input ist eine permutations $ \pi $ over $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, was eine $n $-Variable umkehrbare boolesche Funktion darstellt.
Der Algorithmus führt iterativ die folgenden Schritte aus:

1. Suchen Sie den kleinsten $x $, sodass $x \nE \pi (x) = y $.
2. Suchen von multigesteuerten Toffoli-Vorgängen, die auf die Ausgaben angewendet werden, machen $ \pi (x) = x $ und ändern $ \pi (x ') $ nicht für alle $x ' < x $

## <a name="input"></a>Eingabe

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]

Eine permutations von $2 ^ n $ Elementen, beginnend bei 0.


### <a name="qubits--littleendian"></a>Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Eine Liste von $n $ Qubits, auf die die permutations angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

- [*D. Michael Miller*, *Dmitri Maslov*, *Gerhard W. Dueck*, proc. DAC 2003, IEEE, pp. 318-323, 2003](https://doi.org/10.1145/775832.775915)
- [*Mathias soeken*, *Gerhard W. Dueck*, *D. Michael Miller*, proc. RC 2016, Springer, pp. 307-321, 2016](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Synthese. applypermutationusingzerlegung](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)