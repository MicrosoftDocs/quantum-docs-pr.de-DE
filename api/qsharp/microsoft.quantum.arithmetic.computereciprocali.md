---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Computereciprocali-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: b99e816ed69af6e6d1758442d6f95c5ab0e5c07a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707346"
---
# <a name="computereciprocali-operation"></a>Computereciprocali-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Berechnet die gegenseitige 1/x-Datei für eine Ganzzahl x ohne Vorzeichen unter Verwendung der ganzzahligen Division. Das als ganze Zahl interpretierte Ergebnis ist `floor(2^(2*n-1) / x)` .

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

n-Bit-Ganzzahl ohne Vorzeichen


### <a name="result--littleendian"></a>Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

die 2N-Bit-Ausgabe muss zunächst in "$ \ket $" liegen {0} .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Bei der Eingabe x = 0 ist die Ausgabe alle.