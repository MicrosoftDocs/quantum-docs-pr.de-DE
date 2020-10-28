---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Intstopaulis-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 605257aa7ca39e457127e3c3459b5891145b1863
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701244"
---
# <a name="intstopaulis-function"></a>Intstopaulis-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Konvertiert ein Array von ganzen Zahlen in ein Array von Single-Qubit-Pauli-Operatoren.

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a>Eingabe

### <a name="ints--int"></a>int: [int](xref:microsoft.quantum.lang-ref.int)[]

Array aus ganzen Zahlen im Bereich, der in die `0..3`  Pauli-Operatoren konvertiert werden soll.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Array `paulis` von Pauli-Operatoren mit `Pauli[]` derselben Länge wie `ints` , das `paulis[idxPauli]` gleich dem Element von ist, das `[PauliI, PauliX, PauliY, PauliZ]` von angegeben wird `ints[idxPauli]` .