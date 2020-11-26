---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Intstopaulis-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 2333dcbd2988480e2b2b9b217b26705f3578de00
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230530"
---
# <a name="intstopaulis-function"></a>Intstopaulis-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert ein Array von ganzen Zahlen in ein Array von Single-Qubit-Pauli-Operatoren.

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a>Eingabe

### <a name="ints--int"></a>int: [int](xref:microsoft.quantum.lang-ref.int)[]

Array aus ganzen Zahlen im Bereich, der in die `0..3`  Pauli-Operatoren konvertiert werden soll.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Array `paulis` von Pauli-Operatoren mit `Pauli[]` derselben Länge wie `ints` , das `paulis[idxPauli]` gleich dem Element von ist, das `[PauliI, PauliX, PauliY, PauliZ]` von angegeben wird `ints[idxPauli]` .