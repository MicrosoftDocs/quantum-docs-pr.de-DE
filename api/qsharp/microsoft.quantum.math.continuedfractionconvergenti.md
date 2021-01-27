---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Continuedfractionconvergenti-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c5316c13ce499da88c0d5c45b9d8c5e3a8c6162d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853857"
---
# <a name="continuedfractionconvergenti-function"></a><span data-ttu-id="75a67-102">Continuedfractionconvergenti-Funktion</span><span class="sxs-lookup"><span data-stu-id="75a67-102">ContinuedFractionConvergentI function</span></span>

<span data-ttu-id="75a67-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="75a67-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="75a67-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="75a67-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="75a67-105">Sucht den fortgesetzten Bruchteil konvergent, der sich am nächsten befindet, wenn `fraction` der Nenner kleiner oder gleich ist. `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="75a67-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a><span data-ttu-id="75a67-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="75a67-106">Input</span></span>

### <a name="fraction--fraction"></a><span data-ttu-id="75a67-107">Bruchteil: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="75a67-107">fraction : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>




### <a name="denominatorbound--int"></a><span data-ttu-id="75a67-108">Nenner-gebunden: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="75a67-108">denominatorBound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--fraction"></a><span data-ttu-id="75a67-109">Ausgabe: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="75a67-109">Output : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>

<span data-ttu-id="75a67-110">Fortgesetzter Bruchteil am nächsten, wenn `fraction` der Nenner kleiner oder gleich `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="75a67-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>