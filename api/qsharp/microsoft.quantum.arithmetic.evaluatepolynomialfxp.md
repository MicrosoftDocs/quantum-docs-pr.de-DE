---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Evaluatepolynomialfxp-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: 4f6ed4b34af2e63dd8ee31fb9b93119e06e3ecbc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223186"
---
# <a name="evaluatepolynomialfxp-operation"></a><span data-ttu-id="6ea60-102">Evaluatepolynomialfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6ea60-102">EvaluatePolynomialFxP operation</span></span>

<span data-ttu-id="6ea60-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6ea60-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6ea60-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="6ea60-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="6ea60-105">Wertet ein Polynoms in einer Fixed-Point-Darstellung aus.</span><span class="sxs-lookup"><span data-stu-id="6ea60-105">Evaluates a polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6ea60-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6ea60-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="6ea60-107">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="6ea60-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="6ea60-108">Koeffizienten des polynomds als doppeltes Array, d. h. das Array $ [a_0, A_1,..., a_d] $ für die Polynom$P (x) = a_0 + A_1 x + \cdots + a_d x ^ d $.</span><span class="sxs-lookup"><span data-stu-id="6ea60-108">Coefficients of the polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_d]$ for the polynomial $P(x) = a_0 + a_1 x + \cdots + a_d x^d$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="6ea60-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="6ea60-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="6ea60-110">Eingabe-fest Komma Zahl, für die der polynomwert ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ea60-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="6ea60-111">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="6ea60-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="6ea60-112">Ausgabe feste Punkt Zahl, die $P (x) $ enthält.</span><span class="sxs-lookup"><span data-stu-id="6ea60-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="6ea60-113">Muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6ea60-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6ea60-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6ea60-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

