---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: Applylowdepthand-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 4c5e381227bf82415121add38d0c0d2959fb529d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209314"
---
# <a name="applylowdepthand-operation"></a>Applylowdepthand-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Kehrt ein angegebenes Ziel-Qubit nur dann ein, wenn beide Steuerelement-Qubits den Status 1 aufweisen, mit T-Tiefe 1 und mithilfe von Messungen zum Ausführen der Adjoint-Operation.

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Kehrt `target` nur dann zu, wenn beide Steuerelemente 1 sind, jedoch wird davon ausgegangen, dass `target` sich der Status 0 (null) befindet.  Der Vorgang verfügt über t-count 4, t-Tiefe 1 und erfordert ein Hilfsobjekt und ist daher möglicherweise einem ccnot-Vorgang vorzuziehen, wenn `target` bekanntermaßen 0 ist.  Das Hilfsobjekt dieses Vorgangs ist Messungs basiert und erfordert keine T-Gates und kein Hilfsobjekt.

## <a name="input"></a>Eingabe

### <a name="control1--qubit"></a>Control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit für erstes Steuerelement


### <a name="control2--qubit"></a>Control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit für zweites Steuerelement


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Zusätzliches Qubit für Ziel muss den Status 0 aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

- Cody Jones: "neuartige Konstruktionen für das Fault-tolerante yffoli Gate", Phys. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/physreva. 87.022328
- Peter Selinger: "Quantum-Leitungen von T-tiefen One", Phys. Rev. A 87, 042302, 2013 [arXiv: 1210.0974](https://arxiv.org/abs/1210.0974) doi: 10.1103/physreva. 87.042302