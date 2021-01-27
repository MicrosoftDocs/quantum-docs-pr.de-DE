---
uid: Microsoft.Quantum.Math.PNorm
title: Pnorm-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 6207cca6cda5f9030facd31c327e58bdb9ecbf14
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847654"
---
# <a name="pnorm-function"></a><span data-ttu-id="5321b-102">Pnorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="5321b-102">PNorm function</span></span>

<span data-ttu-id="5321b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="5321b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="5321b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5321b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5321b-105">Gibt die `L(p)` Norm eines Vektors von `Double` s zurück.</span><span class="sxs-lookup"><span data-stu-id="5321b-105">Returns the `L(p)` norm of a vector of `Double`s.</span></span>

<span data-ttu-id="5321b-106">Das heißt, wenn ein Array $x $ vom Typ ist `Double[]` , wird der $p $-Norm $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5321b-106">That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.</span></span>

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a><span data-ttu-id="5321b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5321b-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="5321b-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5321b-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5321b-109">Der Exponent $p $ in der $p $-Norm.</span><span class="sxs-lookup"><span data-stu-id="5321b-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="5321b-110">Array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="5321b-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="5321b-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5321b-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5321b-112">Der $p $-Norm $ \| x \| _P $.</span><span class="sxs-lookup"><span data-stu-id="5321b-112">The $p$-norm $\|x\|_p$.</span></span>