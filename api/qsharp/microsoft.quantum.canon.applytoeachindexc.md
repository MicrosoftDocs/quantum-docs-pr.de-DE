---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexC
title: Applydeeachindexc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexC
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 387d7ea24b9251386a71b42a1f51ce70933bf6fc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704946"
---
# <a name="applytoeachindexc-operation"></a>Applydeeachindexc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.
Der-Modifizierer `C` gibt an, dass der Single-Qubit-Vorgang steuerbar ist.

```qsharp
operation ApplyToEachIndexC<'T> (singleElementOperation : ((Int, 'T) => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="singleelementoperation--intt--unit-ctl"></a>singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Der auf die einzelnen Qubits anzuwendende Vorgang.


### <a name="register--t"></a>Register: 't []

Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, für das jeder der Vorgänge fungiert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyteachindex](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)