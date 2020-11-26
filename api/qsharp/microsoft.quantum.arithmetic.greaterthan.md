---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: GreaterThan-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: 644d68affbdb508938f76de5025a1a463e7284e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223084"
---
# <a name="greaterthan-operation"></a>GreaterThan-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen größer-als-Vergleich zwischen zwei ganzen Zahlen an, die in Qubit-Registern codiert sind, wobei ein Ziel-Qubit basierend auf dem Ergebnis des Vergleichs geflippt wird.

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Führt einen streng größeren Vergleich von zwei Ganzzahlen $x $ und $y $ aus, codiert in Qubit-Register XS und YS. Wenn $x > y $, wird das Ergebnis-Qubit gekippt, andernfalls behält das Qubit-Ergebnis den Zustand bei.

## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian-Qubit-Register Codierung der ersten Ganzzahl $x $.


### <a name="ys--littleendian"></a>YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian Qubit-Register Codierung der zweiten Ganzzahl $y $.


### <a name="result--qubit"></a>Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Einzelnes Qubit, das beim $x > y $ gekippt wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Verwendet den Trick, bei dem $x-y = (x ' + y) ' $, WHERE ' das Einerkomplement bezeichnet.

## <a name="references"></a>Referenzen

- Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton: "A New Quantum Ripple-Carry Additions Circuit", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1

- Thomas Haener, Martin roetteler, Krysta M. svore: "Factoring using 2N + 2 Qubits with Toffoli based modulare Multiplikation", 2016 https://arxiv.org/abs/1611.07995