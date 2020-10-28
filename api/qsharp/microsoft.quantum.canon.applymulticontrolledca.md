---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: Applymulticontrolledca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: 5662efe0dc6f665206b8773596bf885ce631413c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705194"
---
# <a name="applymulticontrolledca-operation"></a>Applymulticontrolledca-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet eine mehrfach gesteuerte Version eines einzeln kontrollierten Vorgangs an.
Der-Modifizierer `CA` gibt an, dass der Single-Qubit-Vorgang steuerbar und adjointable ist.

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="singlycontrolledop--qubit--unit-adj"></a>singlycontrolledop: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein Vorgang, der auf einem einzelnen Qubit gesteuert wird.
Das erste Qubit im-Argument des Vorgangs hat angenommen, dass es sich um ein-Steuerelement handelt, und der Rest wird als Ziel-Qubits angenommen.
`ApplyMultiControlled` Ruft immer `singlyControlledOp` mit einem Argument der Länge von mindestens 1 auf.


### <a name="ccnot--ccnotop"></a>ccnot: [ccnotop](xref:Microsoft.Quantum.Canon.CCNOTop)

Das für die Konstruktion zu verwendende gesteuerte-not-Gate.


### <a name="controls--qubit"></a>Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die Qubits, die `singlyControlledOp` gesteuert werden sollen.
Die Länge von `controls` muss mindestens 1 betragen.


### <a name="targets--qubit"></a>Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die Ziel-Qubits, die auf angewendet werden `singlyControlledOp` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Bei diesem Vorgang werden nur saubere Ancilla-Qubits verwendet.

Eine Erläuterung und ein Leitungs Diagramm finden Sie in Abbildung 4,10, Abschnitt 4,3 in Nielsen & Chuang.

## <a name="references"></a>Referenzen

- [*Michael A. Nielsen, ISAL. Chuang* , Quantum-Berechnung und Quantum-Informationen](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applymulticontrolledc](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)