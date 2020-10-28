---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentL
title: Continuedfractionconvergentl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentL
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: a02b38fedb5b0025f04e7bba86f2f998493206b3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723829"
---
# <a name="continuedfractionconvergentl-function"></a><span data-ttu-id="3b9c3-102">Continuedfractionconvergentl-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b9c3-102">ContinuedFractionConvergentL function</span></span>

<span data-ttu-id="3b9c3-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="3b9c3-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="3b9c3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3b9c3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3b9c3-105">Sucht den fortgesetzten Bruchteil konvergent, der sich am nächsten befindet, wenn `fraction` der Nenner kleiner oder gleich ist. `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="3b9c3-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentL (fraction : Microsoft.Quantum.Math.BigFraction, denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a><span data-ttu-id="3b9c3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3b9c3-106">Input</span></span>

### <a name="fraction--bigfraction"></a><span data-ttu-id="3b9c3-107">Bruchteil: [bigbruchzahl](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="3b9c3-107">fraction : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>




### <a name="denominatorbound--bigint"></a><span data-ttu-id="3b9c3-108">Nenner-gebunden: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3b9c3-108">denominatorBound : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigfraction"></a><span data-ttu-id="3b9c3-109">Ausgabe: [bigbruch](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="3b9c3-109">Output : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>

<span data-ttu-id="3b9c3-110">Fortgesetzter Bruchteil am nächsten, wenn `fraction` der Nenner kleiner oder gleich `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="3b9c3-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>