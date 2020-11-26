---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Squarednorm-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: ecbc66a8851f23187e0c0ea53ce121442323733b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227300"
---
# <a name="squarednorm-function"></a><span data-ttu-id="bfbf3-102">Squarednorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="bfbf3-102">SquaredNorm function</span></span>

<span data-ttu-id="bfbf3-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="bfbf3-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="bfbf3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bfbf3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bfbf3-105">Gibt den quadratischen 2-Norm eines Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="bfbf3-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="bfbf3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfbf3-106">Description</span></span>

<span data-ttu-id="bfbf3-107">Gibt den quadratischen 2-Norm eines Vektors zurück. Das heißt, dass bei Angabe der Eingabe $ \vec{x} $ $ \ sum_i x_i ^ 2 $ zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bfbf3-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="bfbf3-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bfbf3-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="bfbf3-109">Array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="bfbf3-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="bfbf3-110">Der Vektor, dessen Quadrats 2-Norm zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfbf3-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="bfbf3-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bfbf3-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bfbf3-112">Die Quadrat-2-Norm von `array` .</span><span class="sxs-lookup"><span data-stu-id="bfbf3-112">The squared 2-norm of `array`.</span></span>