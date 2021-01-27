---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Multiplyf XP-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 776ccb7a9e1ba1a34b28da6e1cf3a0aafe9da76b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843046"
---
# <a name="multiplyfxp-operation"></a>Multiplyf XP-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Multipliziert zwei Festkomma Zahlen in quantenregistern.

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="fp1--fixedpoint"></a>Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Erste festpunktzahl.


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Zweite Festkomma Zahl.


### <a name="result--fixedpoint"></a>Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Die Ergebnis Festkomma Zahl muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Die aktuelle Implementierung erfordert, dass die drei Fixed-Point-Nummern die gleiche Punktposition und die gleiche Anzahl von Qubits aufweisen.