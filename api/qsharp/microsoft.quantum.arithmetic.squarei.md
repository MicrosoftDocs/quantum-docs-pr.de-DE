---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Squarei-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 79a431d411c4ffd502fb5338b5396341fd63aea8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221860"
---
# <a name="squarei-operation"></a>Squarei-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Berechnet das Quadrat der Ganzzahl `xs` in `result` , das anfänglich NULL sein muss.

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Bit-Nummer zum Quadrat (littleEndian)


### <a name="result--littleendian"></a>Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$2N $-Bit-Ergebnis (littleEndian) muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Verwendet einen standardmäßigen Shift-and-Add-Ansatz, um das Quadrat zu berechnen. Speichert $n-$1-Qubits im Vergleich zur geradlinigen Projekt Mappe, die zuerst XS kopiert, bevor Sie einen regulären Multiplikator anwendet und dann den Kopiervorgang zurücknimmt.