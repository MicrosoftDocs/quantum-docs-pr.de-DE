---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Evaluatepolynomialfxp-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: d88f9002f4ce39b6a16091837c76168fb3a2f086
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843224"
---
# <a name="evaluatepolynomialfxp-operation"></a><span data-ttu-id="2fedd-102">Evaluatepolynomialfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2fedd-102">EvaluatePolynomialFxP operation</span></span>

<span data-ttu-id="2fedd-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2fedd-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2fedd-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="2fedd-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="2fedd-105">Wertet ein Polynoms in einer Fixed-Point-Darstellung aus.</span><span class="sxs-lookup"><span data-stu-id="2fedd-105">Evaluates a polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="2fedd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2fedd-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="2fedd-107">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="2fedd-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="2fedd-108">Koeffizienten des polynomds als doppeltes Array, d. h. das Array $ [a_0, A_1,..., a_d] $ für die Polynom$P (x) = a_0 + A_1 x + \cdots + a_d x ^ d $.</span><span class="sxs-lookup"><span data-stu-id="2fedd-108">Coefficients of the polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_d]$ for the polynomial $P(x) = a_0 + a_1 x + \cdots + a_d x^d$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="2fedd-109">FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2fedd-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2fedd-110">Eingabe-fest Komma Zahl, für die der polynomwert ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fedd-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="2fedd-111">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2fedd-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2fedd-112">Ausgabe feste Punkt Zahl, die $P (x) $ enthält.</span><span class="sxs-lookup"><span data-stu-id="2fedd-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="2fedd-113">Muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2fedd-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2fedd-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2fedd-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

