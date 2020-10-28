---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Squarednorm-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 4165a761753f336cb7b94ad36b11ac324ad4e5c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725020"
---
# <a name="squarednorm-function"></a><span data-ttu-id="a3e69-102">Squarednorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3e69-102">SquaredNorm function</span></span>

<span data-ttu-id="a3e69-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a3e69-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a3e69-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a3e69-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a3e69-105">Gibt den quadratischen 2-Norm eines Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="a3e69-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="a3e69-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3e69-106">Description</span></span>

<span data-ttu-id="a3e69-107">Gibt den quadratischen 2-Norm eines Vektors zurück. Das heißt, dass bei Angabe der Eingabe $ \vec{x} $ $ \ sum_i x_i ^ 2 $ zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3e69-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="a3e69-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3e69-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="a3e69-109">Array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a3e69-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a3e69-110">Der Vektor, dessen Quadrats 2-Norm zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3e69-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="a3e69-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a3e69-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a3e69-112">Die Quadrat-2-Norm von `array` .</span><span class="sxs-lookup"><span data-stu-id="a3e69-112">The squared 2-norm of `array`.</span></span>