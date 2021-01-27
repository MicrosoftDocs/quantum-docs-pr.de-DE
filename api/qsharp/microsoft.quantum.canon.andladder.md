---
uid: Microsoft.Quantum.Canon.AndLadder
title: Andladder-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: AndLadder
qsharp.summary: Performs a controlled "AND ladder" on a register of target qubits.
ms.openlocfilehash: d44c462c7a9fc9521bdecfe2ca7f607e90482baf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845219"
---
# <a name="andladder-operation"></a>Andladder-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt eine gesteuerte "and-Leiter" für ein Register der Ziel-Qubits aus.

```qsharp
operation AndLadder (ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj
```


## <a name="description"></a>Beschreibung

Durch diesen Vorgang wird eine Transformation angewendet, die von der folgenden Zuordnung der Berechnungsbasis beschrieben wird. $ $ \begin{align} \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1, \dots, y \_ {n-1}} \mapsto \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1 \oplus (x \_ 1 \land x \_ 2), \dots, y \_ {n-1} \oplus (x \_ 1 \land x \_ 2 \land \cdots \land x \_ {n-1}}, \end{align} $ $, wobei $ \ket{x \_ 1, \dots, x \_ n} $ bezieht sich auf die Berechnungsbasis Zustände von `controls` , und WHERE $ \ket{y \_ 1, \dots, y \_ {n-1}} $ bezieht sich auf die Berechnungsbasis Zustände von `targets` .

## <a name="input"></a>Eingabe

### <a name="ccnot--ccnotop"></a>ccnot: [ccnotop](xref:Microsoft.Quantum.Canon.CCNOTop)

Das ccnot-Gate, das für die Konstruktion verwendet werden soll.


### <a name="controls--qubit"></a>Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von Qubits, das als Steuerelemente für die-und-Leiter verwendet werden soll.
Mit diesem Vorgang bleiben die Berechnungsbasis Zustände `controls` invariant.
Die Länge von `controls` muss mindestens 2 betragen und muss gleich 1 und der Länge von sein `targets` .


### <a name="targets--qubit"></a>Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die Länge von `targets` muss mindestens 1 betragen und gleich der Länge von minus 1 sein `controls` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

- Wird als Teil von <xref:microsoft.quantum.canon.applymulticontrolledc> und verwendet <xref:microsoft.quantum.canon.applymulticontrolledca> .
- Eine Erläuterung und ein Leitungs Diagramm finden Sie in Abbildung 4,10, Abschnitt 4,3 in Nielsen & Chuang.

## <a name="references"></a>References

- [*Michael A. Nielsen, ISAL. Chuang*, Quantum-Berechnung und Quantum-Informationen](http://doi.org/10.1017/CBO9780511976667)