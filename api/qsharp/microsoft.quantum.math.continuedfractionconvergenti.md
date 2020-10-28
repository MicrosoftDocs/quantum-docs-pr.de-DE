---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Continuedfractionconvergenti-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: 2322e005a5afb73d9719eb65d9ebf50740f1c9fc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723185"
---
# <a name="continuedfractionconvergenti-function"></a><span data-ttu-id="81ebd-102">Continuedfractionconvergenti-Funktion</span><span class="sxs-lookup"><span data-stu-id="81ebd-102">ContinuedFractionConvergentI function</span></span>

<span data-ttu-id="81ebd-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="81ebd-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="81ebd-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="81ebd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="81ebd-105">Sucht den fortgesetzten Bruchteil konvergent, der sich am nächsten befindet, wenn `fraction` der Nenner kleiner oder gleich ist. `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="81ebd-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a><span data-ttu-id="81ebd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81ebd-106">Input</span></span>

### <a name="fraction--fraction"></a><span data-ttu-id="81ebd-107">Bruchteil: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="81ebd-107">fraction : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>




### <a name="denominatorbound--int"></a><span data-ttu-id="81ebd-108">Nenner-gebunden: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="81ebd-108">denominatorBound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--fraction"></a><span data-ttu-id="81ebd-109">Ausgabe: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="81ebd-109">Output : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>

<span data-ttu-id="81ebd-110">Fortgesetzter Bruchteil am nächsten, wenn `fraction` der Nenner kleiner oder gleich `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="81ebd-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>