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
# <a name="evaluateoddpolynomialfxp-operation"></a><span data-ttu-id="51f28-102">Evaluateoddpolynomialfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="51f28-102">EvaluateOddPolynomialFxP operation</span></span>

<span data-ttu-id="51f28-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="51f28-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="51f28-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51f28-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51f28-105">Wertet einen ungeraden Polynoms in einer Fixed-Point-Darstellung aus.</span><span class="sxs-lookup"><span data-stu-id="51f28-105">Evaluates an odd polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="51f28-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="51f28-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="51f28-107">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="51f28-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="51f28-108">Koeffizienten des ungeraden Polynoms als doppeltes Array, d. h. das Array $ [a_0, A_1,..., a_k] $ für die ungeraden Polynoms $P (x) = a_0 x + A_1 x ^ 3 + \cdots + a_k x ^ {2K + 1} $.</span><span class="sxs-lookup"><span data-stu-id="51f28-108">Coefficients of the odd polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the odd polynomial $P(x) = a_0 x + a_1 x^3 + \cdots + a_k x^{2k+1}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="51f28-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="51f28-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="51f28-110">Eingabe-fest Komma Zahl, für die der polynomwert ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51f28-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="51f28-111">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="51f28-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="51f28-112">Ausgabe feste Punkt Zahl, die P (x) enthält.</span><span class="sxs-lookup"><span data-stu-id="51f28-112">Output fixed-point number which will hold P(x).</span></span> <span data-ttu-id="51f28-113">Muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="51f28-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="51f28-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51f28-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

