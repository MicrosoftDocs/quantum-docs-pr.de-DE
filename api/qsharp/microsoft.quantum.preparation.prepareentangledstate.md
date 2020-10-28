---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Prepareentangledstate-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 299d586f7581acdecf22da2f6bbfbb8d45f372f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722177"
---
# <a name="prepareentangledstate-operation"></a>Prepareentangledstate-Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paketen [](https://nuget.org/packages/)


Paar Weise entwinkel zwei Qubit-Register.

Das heißt, wenn zwei Register vorhanden sind, wird der Status "$ \frac {1} {\sqrt {2} } \left (\ket {00} + \ket {11} \right) $" zwischen jedem Paar von Qubits in den entsprechenden Registern vorbereitet, wobei angenommen wird, dass jedes Register im Zustand "$ \ket{0\cdots 0} $" beginnt.

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="left--qubit"></a>Left: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Array im $ \ket{0\cdots 0} $-Status


### <a name="right--qubit"></a>Right: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Array im $ \ket{0\cdots 0} $-Status



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

