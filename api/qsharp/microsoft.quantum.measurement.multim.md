---
uid: Microsoft.Quantum.Measurement.MultiM
title: Multim-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: c39601f3e8b272b9341f1789b4c8e7230cb4182c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226994"
---
# <a name="multim-operation"></a>Multim-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Misst jedes Qubit in einem angegebenen Array standardmäßig.

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a>Eingabe

### <a name="targets--qubit"></a>Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Array von zu messenden Qubits.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__[]

Ein Array von Messergebnissen.