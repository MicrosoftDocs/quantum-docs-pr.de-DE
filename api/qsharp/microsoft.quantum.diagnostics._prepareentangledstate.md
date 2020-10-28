---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 384dad5905cec50b500028e1bc352a742122b299
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702822"
---
# <a name="_prepareentangledstate-operation"></a>_prepareEntangledState Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bei zwei Registern wird der Status der vollständig entkoppelt zwischen jedem Paar von Qubits in den entsprechenden Registern vorbereitet.
Alle Qubits müssen im Zustand | 0 ⟩ beginnen.

Das Ergebnis ist, dass sich die entsprechenden Paare von Qubits aus jedem Register in der $ \bra{\ beta_ {00} } \ket{\ beta_ {00} } $ befinden.

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="left--qubit"></a>Left: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Array im $ \ket{0\cdots 0} $-Status


### <a name="right--qubit"></a>Right: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Array im $ \ket{0\cdots 0} $-Status



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

