---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: ApplyDelta-Parität (Vorgang)
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: bb01eb684ff1820be08a573c0ca6cfc12efeb889
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723983"
---
# <a name="applydeltaparity-operation"></a>ApplyDelta-Parität (Vorgang)

Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)

Paketen [](https://nuget.org/packages/)


Berechnet den Unterschied in der Parität zwischen einem vorherigen pqrs... Begriffe und die nächsten pqrs... zeitig. Dieser Unterschied wird für ein zusätzliches Qubit berechnet.

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit
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



## <a name="remarks"></a>Hinweise

Dabei wird davon ausgegangen, dass die Indizes von P < Q < R < S <... für prevpq und nextpq.