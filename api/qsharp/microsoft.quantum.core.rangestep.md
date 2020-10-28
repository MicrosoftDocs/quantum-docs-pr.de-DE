---
uid: Microsoft.Quantum.Core.RangeStep
title: Rangestep-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: f8e4c42330f2d6afdc1c0a9bdde36081ccab2f94
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702834"
---
# <a name="rangestep-function"></a><span data-ttu-id="e8ea3-102">Rangestep-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8ea3-102">RangeStep function</span></span>

<span data-ttu-id="e8ea3-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="e8ea3-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="e8ea3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8ea3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8ea3-105">Gibt die ganze Zahl zurück, die angibt, wie der nächste Wert eines Bereichs berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e8ea3-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="e8ea3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8ea3-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="e8ea3-107">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="e8ea3-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="e8ea3-108">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e8ea3-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e8ea3-109">Der definierte Schrittwert des angegebenen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="e8ea3-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8ea3-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8ea3-110">Remarks</span></span>

<span data-ttu-id="e8ea3-111">Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.</span><span class="sxs-lookup"><span data-stu-id="e8ea3-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>