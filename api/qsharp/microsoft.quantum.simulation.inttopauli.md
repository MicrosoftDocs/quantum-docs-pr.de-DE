---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: Inttopauli-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: f0f1186f14a0dc30bb34bd29f148cdc830fd1337
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724851"
---
# <a name="inttopauli-function"></a>Inttopauli-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Konvertiert eine ganze Zahl in einen Single-Qubit-Pauli-Operator.

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a>Eingabe

### <a name="idx--int"></a>idx: [int](xref:microsoft.quantum.lang-ref.int)

Ganzzahl im Bereich, der in die `0..3` Pauli-Operatoren konvertiert werden soll.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Ein `Pauli` Operator, der von angegeben wird `[PauliI, PauliX, PauliY, PauliZ][idx]` .