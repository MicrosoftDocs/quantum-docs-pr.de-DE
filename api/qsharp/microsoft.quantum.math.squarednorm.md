---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Squarednorm-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 72ae8266492bef64eaec34cd70c5fe725ee1e8c9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848216"
---
# <a name="squarednorm-function"></a><span data-ttu-id="d21e8-102">Squarednorm-Funktion</span><span class="sxs-lookup"><span data-stu-id="d21e8-102">SquaredNorm function</span></span>

<span data-ttu-id="d21e8-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d21e8-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d21e8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d21e8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d21e8-105">Gibt den quadratischen 2-Norm eines Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="d21e8-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="d21e8-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d21e8-106">Description</span></span>

<span data-ttu-id="d21e8-107">Gibt den quadratischen 2-Norm eines Vektors zurück. Das heißt, dass bei Angabe der Eingabe $ \vec{x} $ $ \ sum_i x_i ^ 2 $ zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d21e8-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="d21e8-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d21e8-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="d21e8-109">Array: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d21e8-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d21e8-110">Der Vektor, dessen Quadrats 2-Norm zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d21e8-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="d21e8-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d21e8-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d21e8-112">Die Quadrat-2-Norm von `array` .</span><span class="sxs-lookup"><span data-stu-id="d21e8-112">The squared 2-norm of `array`.</span></span>