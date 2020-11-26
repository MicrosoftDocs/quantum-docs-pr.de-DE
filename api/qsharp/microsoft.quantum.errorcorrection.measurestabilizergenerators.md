---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: "\"Mess restabilizergenerators\"-Vorgang"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: 6c048c17df21d1026dc671f30d72a13ed8d8b7f5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200627"
---
# <a name="measurestabilizergenerators-operation"></a>"Mess restabilizergenerators"-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Misst den angegebenen Satz von Generatoren einer stabilistabilisgruppe.

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a>Eingabe

### <a name="stabilizergroup--pauli"></a>stabilizergroup: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Ein Array von multiqubit-Pauli-Operatoren.
Beispielsweise `stabilizerGroup[0]` ist eine Liste von Single-Qubit-Pauli-Matrizen, das tensorflow-Produkt, von dem ein stabiliatorgenerator ist.


### <a name="logicalregister--logicalregister"></a>logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Ein Array von Qubits, in denen der stabilikocodecode definiert ist.


### <a name="gadget--pauliqubit--__invalidresult__"></a>Gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ungültig <Result>__ 

Ein Vorgang, der angibt, wie ein multiqubit-Pauli-Operator gemessen werden soll.



## <a name="output--syndrome"></a>Ausgabe:- [Syndrom](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Das Ergebnis der Messungen.

## <a name="remarks"></a>Bemerkungen

Hiermit wird nicht überprüft, ob der angegebene Satz von Generatoren in den einzelnen Generatoren Überlaufen wird.
Wenn keine Überprüfung durchzuführen ist, kann das Ergebnis von Messungen beliebig sein.