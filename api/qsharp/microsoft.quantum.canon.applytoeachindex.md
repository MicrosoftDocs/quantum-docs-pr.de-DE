---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Applydeeachindex-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 4ce184b34add9238e26f9b35b40ec0bddb23ccf9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704954"
---
# <a name="applytoeachindex-operation"></a>Applydeeachindex-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


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