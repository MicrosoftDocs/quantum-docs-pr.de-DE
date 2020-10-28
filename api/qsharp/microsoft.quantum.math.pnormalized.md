---
uid: Microsoft.Quantum.Math.PNormalized
title: Pnormalized-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 6f9dfebe83f52cbf486cd8e6874d3699f5e6b8ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722289"
---
# <a name="pnormalized-function"></a><span data-ttu-id="1bc1b-102">Pnormalized-Funktion</span><span class="sxs-lookup"><span data-stu-id="1bc1b-102">PNormalized function</span></span>

<span data-ttu-id="1bc1b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="1bc1b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="1bc1b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1bc1b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1bc1b-105">Normalisiert einen Vektor von `Double` s in der `L(p)` Norm.</span><span class="sxs-lookup"><span data-stu-id="1bc1b-105">Normalizes a vector of `Double`s in the `L(p)` norm.</span></span>

<span data-ttu-id="1bc1b-106">Das heißt, wenn ein Array $x $ vom Typ ist `Double[]` , wird ein Array zurückgegeben, in dem alle Elemente durch die $p $-Norm $ \| x _P $ dividiert werden \| .</span><span class="sxs-lookup"><span data-stu-id="1bc1b-106">That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.</span></span>

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a><span data-ttu-id="1bc1b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1bc1b-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="1bc1b-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1bc1b-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1bc1b-109">Der Exponent $p $ in der $p $-Norm.</span><span class="sxs-lookup"><span data-stu-id="1bc1b-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="1bc1b-110">Array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="1bc1b-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="1bc1b-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="1bc1b-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="1bc1b-112">Das Array $x $ normalisiert durch die $p $-Norm $ \| x \| _P $.</span><span class="sxs-lookup"><span data-stu-id="1bc1b-112">The array $x$ normalized by the $p$-norm $\|x\|_p$.</span></span>

## <a name="see-also"></a><span data-ttu-id="1bc1b-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1bc1b-113">See Also</span></span>

- [<span data-ttu-id="1bc1b-114">Microsoft. Quantum. Math. pnorm</span><span class="sxs-lookup"><span data-stu-id="1bc1b-114">Microsoft.Quantum.Math.PNorm</span></span>](xref:Microsoft.Quantum.Math.PNorm)