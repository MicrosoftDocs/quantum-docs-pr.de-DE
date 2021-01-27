---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: Inttopauli-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 76f482b86ff4a27b6e6ce6ae4ec3d59422563f12
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842248"
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