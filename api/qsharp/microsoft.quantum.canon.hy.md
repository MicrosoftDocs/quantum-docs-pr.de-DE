---
uid: Microsoft.Quantum.Canon.HY
title: HY-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: HY
qsharp.summary: >-
  Applies the Y-basis analog to the Hadamard transformation that interchanges the Z and Y axes.

  The Y Hadamard transformation $H_Y = S H$ on a single qubit is:

  \begin{align} H_Y \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ i & -i \end{bmatrix}. \end{align}
ms.openlocfilehash: bc3417ff948b718be5b96513f30f3e2714b9e20c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704154"
---
# <a name="hy-operation"></a><span data-ttu-id="82eb6-102">HY-Vorgang</span><span class="sxs-lookup"><span data-stu-id="82eb6-102">HY operation</span></span>

<span data-ttu-id="82eb6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="82eb6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="82eb6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="82eb6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="82eb6-105">Wendet die y-Basis-analog auf die Hadamard-Transformation an, die die Z-und Y-Achse interändert.</span><span class="sxs-lookup"><span data-stu-id="82eb6-105">Applies the Y-basis analog to the Hadamard transformation that interchanges the Z and Y axes.</span></span>

<span data-ttu-id="82eb6-106">Die Y Hadamard-Transformation $H _Y = S H $ für ein einzelnes Qubit ist:</span><span class="sxs-lookup"><span data-stu-id="82eb6-106">The Y Hadamard transformation $H_Y = S H$ on a single qubit is:</span></span>

<span data-ttu-id="82eb6-107">\begin{align} H_Y \mathrel{: =} \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ i &-i \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="82eb6-107">\begin{align} H_Y \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ i & -i \end{bmatrix}.</span></span>
<span data-ttu-id="82eb6-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="82eb6-108">\end{align}</span></span>

```qsharp
operation HY (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="82eb6-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="82eb6-109">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="82eb6-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="82eb6-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="82eb6-111">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="82eb6-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="82eb6-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82eb6-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="82eb6-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82eb6-113">See Also</span></span>

- [<span data-ttu-id="82eb6-114">Microsoft. Quantum. intrinsisch. H</span><span class="sxs-lookup"><span data-stu-id="82eb6-114">Microsoft.Quantum.Intrinsic.H</span></span>](xref:Microsoft.Quantum.Intrinsic.H)