---
uid: Microsoft.Quantum.Math.PNormalized
title: Pnormalized-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: ea6a88d07d3b246f666b793f0b10ab6598ea4ff6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854845"
---
# <a name="pnormalized-function"></a><span data-ttu-id="35292-102">Pnormalized-Funktion</span><span class="sxs-lookup"><span data-stu-id="35292-102">PNormalized function</span></span>

<span data-ttu-id="35292-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="35292-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="35292-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="35292-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="35292-105">Normalisiert einen Vektor von `Double` s in der `L(p)` Norm.</span><span class="sxs-lookup"><span data-stu-id="35292-105">Normalizes a vector of `Double`s in the `L(p)` norm.</span></span>

<span data-ttu-id="35292-106">Das heißt, wenn ein Array $x $ vom Typ ist `Double[]` , wird ein Array zurückgegeben, in dem alle Elemente durch die $p $-Norm $ \| x _P $ dividiert werden \| .</span><span class="sxs-lookup"><span data-stu-id="35292-106">That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.</span></span>

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a><span data-ttu-id="35292-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="35292-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="35292-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="35292-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="35292-109">Der Exponent $p $ in der $p $-Norm.</span><span class="sxs-lookup"><span data-stu-id="35292-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="35292-110">Array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="35292-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="35292-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="35292-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="35292-112">Das Array $x $ normalisiert durch die $p $-Norm $ \| x \| _P $.</span><span class="sxs-lookup"><span data-stu-id="35292-112">The array $x$ normalized by the $p$-norm $\|x\|_p$.</span></span>

## <a name="see-also"></a><span data-ttu-id="35292-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="35292-113">See Also</span></span>

- [<span data-ttu-id="35292-114">Microsoft. Quantum. Math. pnorm</span><span class="sxs-lookup"><span data-stu-id="35292-114">Microsoft.Quantum.Math.PNorm</span></span>](xref:Microsoft.Quantum.Math.PNorm)