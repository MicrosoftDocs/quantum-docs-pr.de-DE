---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Continuedfractionconvergenti-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: d37bf1c10899d06e798d29c68f88b06f2d5918a9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195561"
---
# <a name="continuedfractionconvergenti-function"></a><span data-ttu-id="31bb0-102">Continuedfractionconvergenti-Funktion</span><span class="sxs-lookup"><span data-stu-id="31bb0-102">ContinuedFractionConvergentI function</span></span>

<span data-ttu-id="31bb0-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="31bb0-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="31bb0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="31bb0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="31bb0-105">Sucht den fortgesetzten Bruchteil konvergent, der sich am nächsten befindet, wenn `fraction` der Nenner kleiner oder gleich ist. `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="31bb0-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a><span data-ttu-id="31bb0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="31bb0-106">Input</span></span>

### <a name="fraction--fraction"></a><span data-ttu-id="31bb0-107">Bruchteil: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="31bb0-107">fraction : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>




### <a name="denominatorbound--int"></a><span data-ttu-id="31bb0-108">Nenner-gebunden: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31bb0-108">denominatorBound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--fraction"></a><span data-ttu-id="31bb0-109">Ausgabe: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="31bb0-109">Output : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>

<span data-ttu-id="31bb0-110">Fortgesetzter Bruchteil am nächsten, wenn `fraction` der Nenner kleiner oder gleich `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="31bb0-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>