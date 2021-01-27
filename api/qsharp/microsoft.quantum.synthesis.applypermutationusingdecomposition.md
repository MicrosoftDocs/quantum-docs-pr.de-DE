---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition
title: Applypermutationusingzerlegungs-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecomposition
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 765b6d301363021f5b57a22f90e2ada38c9c09ec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857392"
---
# <a name="applypermutationusingdecomposition-operation"></a>Applypermutationusingzerlegungs-Vorgang

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Pertrauert die Verstärkung in einem Quantum-Zustand, wenn eine permutations mithilfe der Zerlegungs basierten Synthese verwendet wird.

```qsharp
operation ApplyPermutationUsingDecomposition (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschreibung

Mit dieser Prozedur wird der Ansatz der Zerlegungs basierten Synthese implementiert.  Die Eingabe ist eine permutations $ \pi $ over $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, was eine $n $-Variable umkehrbare boolesche Funktion darstellt.
Der Algorithmus führt iterativ die folgenden Schritte für jeden Variablen Index aus $i $:

1. Compute $ ((\ pi_l, \ pi_r), \pi ') $ so, dass die Bilder von $ \ pi_l $ und $ \ pi_r $ keine Bits in ihren Elementen in anderen Indizes als $i $ und Bilder von $ \pi ' $ do not Change Bit $i $ in ihren Elementen ändern.
2. Legen Sie $ \pi \leftpfeil \pi ' $, und leiten Sie Wahrheitstabellen aus $ \ pi_l $ und $ \ pi_r $ auf der Grundlage von Elementen, die keine Festpunkte sind, ab.

Nachdem Sie diese Schritte für alle Variablen Indizes ausgeführt haben, ist die verbleibende permutations $ \pi $ die Identität. basierend auf den gesammelten Wahrheitstabellen und-Indizes kann eine durch Wahrheitstabelle kontrollierte @"microsoft.quantum.intrinsic.x" Vorgänge mithilfe des-Vorgangs angewendet werden @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" .

Die Reihenfolge der Variablen ist $0, \dots, n-$1.  Eine benutzerdefinierte Reihenfolge der Variablen kann im Vorgang angegeben werden @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder" .

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
  ApplyPermutationUsingDecomposition([0, 2, 1, 3], LittleEndian(qubits));
}
```

## <a name="references"></a>References

- [*Alexis de Vos*, *Yvan Van Rentergem*, ADV. in Math. of comm. 2 (2), 2008, pp. 183--200](http://www.aimsciences.org/article/doi/10.3934/amc.2008.2.183)
- [*Mathias soeken*, *Laura tague*, *Gerhard W. Dueck*, *Rolf Drechsler*, Journal der symbolischen Berechnung 73 (2016), pp. 1--26](https://www.sciencedirect.com/science/article/pii/S0747717115000188?via%3Dihub)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Synthese. applypermutationusingumcompositionwithvariableorder](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder)
- [Microsoft. Quantum. Synthese. applypermutationusingtransformation](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)