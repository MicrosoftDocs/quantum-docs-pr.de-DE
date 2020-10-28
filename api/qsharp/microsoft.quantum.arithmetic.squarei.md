---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Squarei-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: d7334d50f245ba358624e6e2eee94b63d9ed7569
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706223"
---
# <a name="squarei-operation"></a>Squarei-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Berechnet das Quadrat der Ganzzahl `xs` in `result` , das anfänglich NULL sein muss.

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Bit-Nummer zum Quadrat (littleEndian)


### <a name="result--littleendian"></a>Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$2N $-Bit-Ergebnis (littleEndian) muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Verwendet einen standardmäßigen Shift-and-Add-Ansatz, um das Quadrat zu berechnen. Speichert $n-$1-Qubits im Vergleich zur geradlinigen Projekt Mappe, die zuerst XS kopiert, bevor Sie einen regulären Multiplikator anwendet und dann den Kopiervorgang zurücknimmt.