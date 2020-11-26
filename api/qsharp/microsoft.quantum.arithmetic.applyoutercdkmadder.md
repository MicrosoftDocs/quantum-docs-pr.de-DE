---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Applyoutercdkmadder-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: 81311a75beedb62331184faf4e1523f3ccc74f43
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190665"
---
# <a name="applyoutercdkmadder-operation"></a>Applyoutercdkmadder-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Umkehrbarer, direkter Ripple-Operation-Vorgang, der in der ganzzahligen Additions Operation ripplecarryaddercdkm weiter unten verwendet wird.
Bei zwei Qubit `xs` -Registern und `ys` derselben Länge wendet der-Vorgang eine Ripple-Sequenz Sequenz von "CNOT" und "ccnot Gates" mit Qubits in `xs` und als die Ziele an `ys` `xs` .

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Erstes Qubit-Register, das Steuerelemente und Ziele enthält.


### <a name="ys--littleendian"></a>YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Zweites Qubit-Register, das zu den Steuerelementen beiträgt.


### <a name="ancilla--qubit"></a>Ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das in ripplecarryaddercdkm verwendete Ancilla-Qubit, das an diesen Vorgang übergeben wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

- Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton: "A New Quantum Ripple-Carry Additions Circuit", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1