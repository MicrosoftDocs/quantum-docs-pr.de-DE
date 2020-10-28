---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Applydeeach-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: e1625829e2e9efd9d39fe0692f01c1cbbffc651c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704983"
---
# <a name="applytoeach-operation"></a>Applydeeach-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="singleelementoperation--t--unit"></a>singleelementoperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Der auf die einzelnen Qubits anzuwendende Vorgang.


### <a name="register--t"></a>Register: 't []

Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, für das der Vorgang fungiert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyumeachc](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [Microsoft. Quantum. Canon. applyumeacha](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [Microsoft. Quantum. Canon. applyumeachca](xref:Microsoft.Quantum.Canon.ApplyToEachCA)