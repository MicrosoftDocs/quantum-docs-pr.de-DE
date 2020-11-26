---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: ApplyDelta-Parität (Vorgang)
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: 40157b6a166b09c6fee63d86e203f92069d008f1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225753"
---
# <a name="applydeltaparity-operation"></a>ApplyDelta-Parität (Vorgang)

Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)

Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Berechnet den Unterschied in der Parität zwischen einem vorherigen pqrs... Begriffe und die nächsten pqrs... zeitig. Dieser Unterschied wird für ein zusätzliches Qubit berechnet.

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="prevfermionicterm--int"></a>prevfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]

Liste der Indizes für vorherige pqrs... Bedingungen.


### <a name="nextfermionicterm--int"></a>nextfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]

Liste der Indizes für die nächsten pqrs... Bedingungen.


### <a name="aux--qubit"></a>AUX: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein zusätzliches Qubit, auf das die Ergebnisse der Paritäts Berechnung gespeichert werden.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit wurde von allen pqrs bearbeitet... Bedingungen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Dabei wird davon ausgegangen, dass die Indizes von P < Q < R < S <... für prevpq und nextpq.