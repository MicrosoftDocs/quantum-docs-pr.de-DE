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
# <a name="evaluatepolynomialfxp-operation"></a><span data-ttu-id="487c5-102">Evaluatepolynomialfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="487c5-102">EvaluatePolynomialFxP operation</span></span>

<span data-ttu-id="487c5-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="487c5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="487c5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="487c5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="487c5-105">Wertet ein Polynoms in einer Fixed-Point-Darstellung aus.</span><span class="sxs-lookup"><span data-stu-id="487c5-105">Evaluates a polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="487c5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="487c5-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="487c5-107">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="487c5-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="487c5-108">Koeffizienten des polynomds als doppeltes Array, d. h. das Array $ [a_0, A_1,..., a_d] $ für die Polynom$P (x) = a_0 + A_1 x + \cdots + a_d x ^ d $.</span><span class="sxs-lookup"><span data-stu-id="487c5-108">Coefficients of the polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_d]$ for the polynomial $P(x) = a_0 + a_1 x + \cdots + a_d x^d$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="487c5-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="487c5-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="487c5-110">Eingabe-fest Komma Zahl, für die der polynomwert ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="487c5-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="487c5-111">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="487c5-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="487c5-112">Ausgabe feste Punkt Zahl, die $P (x) $ enthält.</span><span class="sxs-lookup"><span data-stu-id="487c5-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="487c5-113">Muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="487c5-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="487c5-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="487c5-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

