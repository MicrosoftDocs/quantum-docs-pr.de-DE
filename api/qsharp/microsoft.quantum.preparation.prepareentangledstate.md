---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Prepareentangledstate-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 9bf42131860b9fe9bd223ade32f95ec747abefe8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854363"
---
# <a name="prepareentangledstate-operation"></a>Prepareentangledstate-Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Paar Weise entwinkel zwei Qubit-Register.

Das heißt, wenn zwei Register vorhanden sind, wird der Status "$ \frac {1} {\sqrt {2} } \left (\ket {00} + \ket {11} \right) $" zwischen jedem Paar von Qubits in den entsprechenden Registern vorbereitet, wobei angenommen wird, dass jedes Register im Zustand "$ \ket{0\cdots 0} $" beginnt.

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="left--qubit"></a>Left: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Array im $ \ket{0\cdots 0} $-Status


### <a name="right--qubit"></a>Right: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Array im $ \ket{0\cdots 0} $-Status



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

