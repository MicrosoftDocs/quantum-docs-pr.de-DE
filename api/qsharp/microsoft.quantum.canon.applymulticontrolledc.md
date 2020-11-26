---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledC
title: Applymulticontrolledc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledC
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 2d5703eed3a3b6e611ae7c993febf018fcb148b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218409"
---
# <a name="applymulticontrolledc-operation"></a>Applymulticontrolledc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet eine mehrfach gesteuerte Version eines einzeln kontrollierten Vorgangs an.
Der-Modifizierer `C` gibt an, dass der Single-Qubit-Vorgang steuerbar ist.

```qsharp
operation ApplyMultiControlledC (singlyControlledOp : (Qubit[] => Unit), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Eingabe

### <a name="singlycontrolledop--qubit--unit"></a>singlycontrolledop: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang, der auf einem einzelnen Qubit gesteuert wird.
Bei dem ersten Qubit im-Argument des Vorgangs wird angenommen, dass es sich um ein-Steuerelement handelt, und der Rest wird als Ziel-Qubits angenommen.
`ApplyMultiControlled` Ruft immer `singlyControlledOp` mit einem Argument der Länge von mindestens 1 auf.


### <a name="ccnot--ccnotop"></a>ccnot: [ccnotop](xref:Microsoft.Quantum.Canon.CCNOTop)

Das für die Konstruktion zu verwendende gesteuerte-not-Gate.


### <a name="controls--qubit"></a>Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die Qubits, die `singlyControlledOp` gesteuert werden sollen.
Die Länge von `controls` muss mindestens 1 betragen.


### <a name="targets--qubit"></a>Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die Ziel-Qubits, die auf angewendet werden `singlyControlledOp` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Bei diesem Vorgang werden nur saubere Ancilla-Qubits verwendet.

Eine Erläuterung und ein Leitungs Diagramm finden Sie in Abbildung 4,10, Abschnitt 4,3 in Nielsen & Chuang.

## <a name="references"></a>Referenzen

- [*Michael A. Nielsen, ISAL. Chuang*, Quantum-Berechnung und Quantum-Informationen](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applymulticontrolledca](xref:Microsoft.Quantum.Canon.ApplyMultiControlledCA)