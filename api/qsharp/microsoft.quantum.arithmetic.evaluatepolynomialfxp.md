---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Evaluatepolynomialfxp-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: 3903bf69d5b0a6e57530f2c6a44e1d351c8a605f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707319"
---
# <a name="evaluatepolynomialfxp-operation"></a>Evaluatepolynomialfxp-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Wertet ein Polynoms in einer Fixed-Point-Darstellung aus.

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a>Eingabe

### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Koeffizienten des polynomds als doppeltes Array, d. h. das Array $ [a_0, A_1,..., a_d] $ für die Polynom$P (x) = a_0 + A_1 x + \cdots + a_d x ^ d $.


### <a name="fpx--fixedpoint"></a>FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Eingabe-fest Komma Zahl, für die der polynomwert ausgewertet werden soll.


### <a name="result--fixedpoint"></a>Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Ausgabe feste Punkt Zahl, die $P (x) $ enthält. Muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

