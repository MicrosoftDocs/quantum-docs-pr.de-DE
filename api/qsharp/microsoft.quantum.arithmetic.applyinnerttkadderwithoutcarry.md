---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdderWithoutCarry
title: Applyinnerttkadderwithoutcarry-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdderWithoutCarry
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 656dc947ab88a7e7f1e8e8722c5262470307f7dc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190954"
---
# <a name="applyinnerttkadderwithoutcarry-operation"></a>Applyinnerttkadderwithoutcarry-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementiert die innere Additions Funktion für den Vorgang ripplecarryaddernocarryttk. Dies ist der innere Vorgang, der mit dem äußeren Vorgang konjuregiert wird, um den vollständigen Adder zu konstruieren.

```qsharp
operation ApplyInnerTTKAdderWithoutCarry (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

"LittleEndian Qubit": Codierung der ersten ganzzahligen Summe und Eingabe in ripplecarryaddernocarryttk.


### <a name="ys--littleendian"></a>YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian Qubit-Register Codierung der zweiten ganzzahligen Summe und Eingabe in ripplecarryaddernocarryttk.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Der angegebene kontrollierte Vorgang verwendet die Symmetrie und den gegenseitigen Abbruch von Vorgängen, um die Standard Implementierung zu verbessern, mit der jedem Vorgang ein Steuerelement hinzugefügt wird.

## <a name="references"></a>Referenzen

- Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Additions-und ungebundene Fan-Out", Quantum-Informationen und-Berechnung, Vol. 10, 2010.
  https://arxiv.org/abs/0910.2530