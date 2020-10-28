---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Dividei-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 0cc16dddc27a000dbc30de6ae27976a01fd9f4ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707343"
---
# <a name="dividei-operation"></a>Dividei-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Dividiert zwei Quantum-Ganzzahlen.

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>BESCHREIBUNG

`xs` hält den Rest `xs - floor(xs/ys) * ys` und `result` hält `floor(xs/ys)` .

## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Bit-Dividende wird durch den Rest ersetzt.


### <a name="ys--littleendian"></a>YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Bit-Divisor


### <a name="result--littleendian"></a>Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Bit-Ergebnis muss zunächst den Status $ \ket {0} $ aufweisen und durch das Ergebnis der ganzzahligen Division ersetzt werden.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Verwendet einen standardmäßigen Shift-and-Subtract-Ansatz, um die Division zu implementieren.
Die kontrollierte Version ist spezialisiert, sodass für die Subtraktion keine zusätzlichen Steuerelemente erforderlich sind.