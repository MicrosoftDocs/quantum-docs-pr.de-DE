---
uid: Microsoft.Quantum.Measurement.MultiM
title: Multim-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: b7f4083bde84c204611ea33746ae351a3e27b946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857008"
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