---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterTTKAdder
title: Applyouterttkadder-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterTTKAdder
qsharp.summary: Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.
ms.openlocfilehash: aed15a4d1f3ca7121d6da665f5c08442fd495619
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190614"
---
# <a name="applyouterttkadder-operation"></a>Applyouterttkadder-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementiert den äußeren Vorgang für ripplecarryadderttk, um den inneren Vorgang zum Erstellen des vollständigen Adder konjugieren.

```qsharp
operation ApplyOuterTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian-Qubit-Registrierung Codieren der ersten ganzzahligen Summe und Eingabe in ripplecarryadderttk.


### <a name="ys--littleendian"></a>YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian Qubit-Register Codierung der zweiten ganzzahligen Summe und Eingabe in ripplecarryadderttk.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

- Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Additions-und ungebundene Fan-Out", Quantum-Informationen und-Berechnung, Vol. 10, 2010.
  https://arxiv.org/abs/0910.2530