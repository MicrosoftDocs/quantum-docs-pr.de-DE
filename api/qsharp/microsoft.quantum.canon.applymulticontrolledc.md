---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledC
title: Applymulticontrolledc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledC
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: bf6b78cd18a827a9a4fd9d61dfd4d240de3503e9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844866"
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

## <a name="references"></a>References

- [*Michael A. Nielsen, ISAL. Chuang*, Quantum-Berechnung und Quantum-Informationen](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applymulticontrolledca](xref:Microsoft.Quantum.Canon.ApplyMultiControlledCA)