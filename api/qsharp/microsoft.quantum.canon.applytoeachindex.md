---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Applydeeachindex-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 8b34dc24580a3df7ae2c13ef87a6fa10c7afd3f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844591"
---
# <a name="applytoeachindex-operation"></a>Applydeeachindex-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="singleelementoperation--intt--unit"></a>singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Der auf die einzelnen Qubits anzuwendende Vorgang.


### <a name="register--t"></a>Register: 't []

Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, für das jeder der Vorgänge fungiert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyyeach](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [Microsoft. Quantum. Canon. applyteachindexa](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [Microsoft. Quantum. Canon. applyteachindexc](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [Microsoft. Quantum. Canon. applyteachindexca](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)