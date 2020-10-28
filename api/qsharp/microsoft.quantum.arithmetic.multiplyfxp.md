---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Multiplyf XP-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 18883f3f4c3793b91e248f4bd89f9def640bf254
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706383"
---
# <a name="multiplyfxp-operation"></a>Multiplyf XP-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Multipliziert zwei Festkomma Zahlen in quantenregistern.

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a>Eingabe

### <a name="fp1--fixedpoint"></a>Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Erste festpunktzahl.


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Zweite Festkomma Zahl.


### <a name="result--fixedpoint"></a>Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Die Ergebnis Festkomma Zahl muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Die aktuelle Implementierung erfordert, dass die drei Fixed-Point-Nummern die gleiche Punktposition und die gleiche Anzahl von Qubits aufweisen.