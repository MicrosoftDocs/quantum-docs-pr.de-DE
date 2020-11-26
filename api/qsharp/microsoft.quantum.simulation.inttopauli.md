---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: Inttopauli-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 18edb600f7b5b33c7ad98e78e32903c570082225
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229204"
---
# <a name="inttopauli-function"></a>Inttopauli-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert eine ganze Zahl in einen Single-Qubit-Pauli-Operator.

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a>Eingabe

### <a name="idx--int"></a>idx: [int](xref:microsoft.quantum.lang-ref.int)

Ganzzahl im Bereich, der in die `0..3` Pauli-Operatoren konvertiert werden soll.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Ein `Pauli` Operator, der von angegeben wird `[PauliI, PauliX, PauliY, PauliZ][idx]` .