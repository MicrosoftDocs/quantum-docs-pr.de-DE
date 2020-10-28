---
uid: Microsoft.Quantum.Math.PNorm
title: Pnorm-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: cea85715e448305486f6d8a6c10e11da56edf3ee
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722303"
---
# <a name="pnorm-function"></a><span data-ttu-id="62205-102">Pnorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="62205-102">PNorm function</span></span>

<span data-ttu-id="62205-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="62205-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="62205-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="62205-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="62205-105">Gibt die `L(p)` Norm eines Vektors von `Double` s zurück.</span><span class="sxs-lookup"><span data-stu-id="62205-105">Returns the `L(p)` norm of a vector of `Double`s.</span></span>

<span data-ttu-id="62205-106">Das heißt, wenn ein Array $x $ vom Typ ist `Double[]` , wird der $p $-Norm $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62205-106">That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.</span></span>

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a><span data-ttu-id="62205-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="62205-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="62205-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="62205-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="62205-109">Der Exponent $p $ in der $p $-Norm.</span><span class="sxs-lookup"><span data-stu-id="62205-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="62205-110">Array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="62205-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="62205-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="62205-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="62205-112">Der $p $-Norm $ \| x \| _P $.</span><span class="sxs-lookup"><span data-stu-id="62205-112">The $p$-norm $\|x\|_p$.</span></span>