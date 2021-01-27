---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: Applypermutationusingtransformation-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: 79913bec44514d477b7ee0668b43396b297b9ab8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858997"
---
# <a name="applypermutationusingtransformation-operation"></a>Applypermutationusingtransformation-Vorgang

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Pertrauert die Verstärkung in einem Quantum-Zustand, wenn eine permutations mithilfe der Transformations basierten Synthese verwendet wird.

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschreibung

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



## <a name="example"></a>Beispiel

So können Sie einen `SWAP` Vorgang synthetisieren:

```qsharp
using (qubits = Qubit[2]) {
  ApplyPermutationUsingTransformation([0, 2, 1, 3], LittleEndian(qubits));
}
```

## <a name="references"></a>References

- [*D. Michael Miller*, *Dmitri Maslov*, *Gerhard W. Dueck*, proc. DAC 2003, IEEE, pp. 318-323, 2003](https://doi.org/10.1145/775832.775915)
- [*Mathias soeken*, *Gerhard W. Dueck*, *D. Michael Miller*, proc. RC 2016, Springer, pp. 307-321, 2016](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Synthese. applypermutationusingzerlegung](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)