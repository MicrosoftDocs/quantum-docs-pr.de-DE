---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Evaluateoddpolynomialfxp-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: 1bf9b6e7c416e994e70b93e5967caefd444f6426
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223220"
---
# <a name="evaluateoddpolynomialfxp-operation"></a><span data-ttu-id="b40f6-102">Evaluateoddpolynomialfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b40f6-102">EvaluateOddPolynomialFxP operation</span></span>

<span data-ttu-id="b40f6-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b40f6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b40f6-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="b40f6-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="b40f6-105">Wertet einen ungeraden Polynoms in einer Fixed-Point-Darstellung aus.</span><span class="sxs-lookup"><span data-stu-id="b40f6-105">Evaluates an odd polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b40f6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b40f6-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="b40f6-107">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b40f6-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b40f6-108">Koeffizienten des ungeraden Polynoms als doppeltes Array, d. h. das Array $ [a_0, A_1,..., a_k] $ für die ungeraden Polynoms $P (x) = a_0 x + A_1 x ^ 3 + \cdots + a_k x ^ {2K + 1} $.</span><span class="sxs-lookup"><span data-stu-id="b40f6-108">Coefficients of the odd polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the odd polynomial $P(x) = a_0 x + a_1 x^3 + \cdots + a_k x^{2k+1}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="b40f6-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="b40f6-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="b40f6-110">Eingabe-fest Komma Zahl, für die der polynomwert ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b40f6-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="b40f6-111">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="b40f6-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="b40f6-112">Ausgabe feste Punkt Zahl, die P (x) enthält.</span><span class="sxs-lookup"><span data-stu-id="b40f6-112">Output fixed-point number which will hold P(x).</span></span> <span data-ttu-id="b40f6-113">Muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b40f6-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b40f6-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b40f6-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

