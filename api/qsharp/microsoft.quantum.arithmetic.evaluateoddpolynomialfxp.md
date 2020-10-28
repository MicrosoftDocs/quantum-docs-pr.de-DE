---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Evaluateoddpolynomialfxp-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: d52da4092f16d43ab9d08b03f798a4d6789c7348
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707327"
---
# <a name="evaluateoddpolynomialfxp-operation"></a>Evaluateoddpolynomialfxp-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Wertet einen ungeraden Polynoms in einer Fixed-Point-Darstellung aus.

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a>Eingabe

### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Koeffizienten des ungeraden Polynoms als doppeltes Array, d. h. das Array $ [a_0, A_1,..., a_k] $ für die ungeraden Polynoms $P (x) = a_0 x + A_1 x ^ 3 + \cdots + a_k x ^ {2K + 1} $.


### <a name="fpx--fixedpoint"></a>FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Eingabe-fest Komma Zahl, für die der polynomwert ausgewertet werden soll.


### <a name="result--fixedpoint"></a>Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Ausgabe feste Punkt Zahl, die P (x) enthält. Muss zunächst den Status $ \ket {0} $ aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

