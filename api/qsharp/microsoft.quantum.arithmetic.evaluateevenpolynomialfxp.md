---
uid: Microsoft.Quantum.Arithmetic.EvaluateEvenPolynomialFxP
title: Evaluateevenpolynomialfxp-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateEvenPolynomialFxP
qsharp.summary: Evaluates an even polynomial in a fixed-point representation.
ms.openlocfilehash: e49a6d47553a60766b561525e8cfa37e95fda9e8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707330"
---
# <a name="evaluateevenpolynomialfxp-operation"></a><span data-ttu-id="51c49-102">Evaluateevenpolynomialfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="51c49-102">EvaluateEvenPolynomialFxP operation</span></span>

<span data-ttu-id="51c49-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="51c49-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="51c49-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51c49-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51c49-105">Wertet ein sogar polynomal in einer Fixed-Point-Darstellung aus.</span><span class="sxs-lookup"><span data-stu-id="51c49-105">Evaluates an even polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateEvenPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="51c49-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="51c49-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="51c49-107">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="51c49-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="51c49-108">Koeffizienten der geraden Polynomen als Double-Array, d. h. das Array $ [a_0, A_1,..., a_k] $ für die gerade Polynom$P (x) = a_0 + A_1 x ^ 2 + \cdots + a_k x ^ {2K} $.</span><span class="sxs-lookup"><span data-stu-id="51c49-108">Coefficients of the even polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the even polynomial $P(x) = a_0 + a_1 x^2 + \cdots + a_k x^{2k}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="51c49-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="51c49-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="51c49-110">Eingabe-fest Komma Zahl, für die der polynomwert ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51c49-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="51c49-111">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="51c49-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="51c49-112">Ausgabe feste Punkt Zahl, die $P (x) $ enthält.</span><span class="sxs-lookup"><span data-stu-id="51c49-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="51c49-113">Muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="51c49-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="51c49-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51c49-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

