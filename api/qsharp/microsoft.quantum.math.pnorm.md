---
uid: Microsoft.Quantum.Math.PNorm
title: Pnorm-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 3fe029bd893fc4d11aaf351f7ea566256cac5a9e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194728"
---
# <a name="pnorm-function"></a><span data-ttu-id="31d74-102">Pnorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="31d74-102">PNorm function</span></span>

<span data-ttu-id="31d74-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="31d74-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="31d74-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="31d74-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="31d74-105">Gibt die `L(p)` Norm eines Vektors von `Double` s zurück.</span><span class="sxs-lookup"><span data-stu-id="31d74-105">Returns the `L(p)` norm of a vector of `Double`s.</span></span>

<span data-ttu-id="31d74-106">Das heißt, wenn ein Array $x $ vom Typ ist `Double[]` , wird der $p $-Norm $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="31d74-106">That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.</span></span>

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a><span data-ttu-id="31d74-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="31d74-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="31d74-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="31d74-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="31d74-109">Der Exponent $p $ in der $p $-Norm.</span><span class="sxs-lookup"><span data-stu-id="31d74-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="31d74-110">Array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="31d74-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="31d74-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="31d74-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="31d74-112">Der $p $-Norm $ \| x \| _P $.</span><span class="sxs-lookup"><span data-stu-id="31d74-112">The $p$-norm $\|x\|_p$.</span></span>