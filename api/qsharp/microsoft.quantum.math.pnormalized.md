---
uid: Microsoft.Quantum.Math.PNormalized
title: Pnormalized-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 196bdab67528aa8672a010ac3830459e27276ce9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227521"
---
# <a name="pnormalized-function"></a><span data-ttu-id="2a5b7-102">Pnormalized-Funktion</span><span class="sxs-lookup"><span data-stu-id="2a5b7-102">PNormalized function</span></span>

<span data-ttu-id="2a5b7-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2a5b7-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2a5b7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2a5b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2a5b7-105">Normalisiert einen Vektor von `Double` s in der `L(p)` Norm.</span><span class="sxs-lookup"><span data-stu-id="2a5b7-105">Normalizes a vector of `Double`s in the `L(p)` norm.</span></span>

<span data-ttu-id="2a5b7-106">Das heißt, wenn ein Array $x $ vom Typ ist `Double[]` , wird ein Array zurückgegeben, in dem alle Elemente durch die $p $-Norm $ \| x _P $ dividiert werden \| .</span><span class="sxs-lookup"><span data-stu-id="2a5b7-106">That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.</span></span>

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a><span data-ttu-id="2a5b7-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a5b7-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="2a5b7-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2a5b7-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2a5b7-109">Der Exponent $p $ in der $p $-Norm.</span><span class="sxs-lookup"><span data-stu-id="2a5b7-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="2a5b7-110">Array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="2a5b7-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="2a5b7-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="2a5b7-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="2a5b7-112">Das Array $x $ normalisiert durch die $p $-Norm $ \| x \| _P $.</span><span class="sxs-lookup"><span data-stu-id="2a5b7-112">The array $x$ normalized by the $p$-norm $\|x\|_p$.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a5b7-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2a5b7-113">See Also</span></span>

- [<span data-ttu-id="2a5b7-114">Microsoft. Quantum. Math. pnorm</span><span class="sxs-lookup"><span data-stu-id="2a5b7-114">Microsoft.Quantum.Math.PNorm</span></span>](xref:Microsoft.Quantum.Math.PNorm)