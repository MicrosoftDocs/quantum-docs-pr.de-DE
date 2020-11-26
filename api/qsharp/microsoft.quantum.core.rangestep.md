---
uid: Microsoft.Quantum.Core.RangeStep
title: Rangestep-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: 39c8581fe795a1b76d2a6e81c238a271287c2c38
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213802"
---
# <a name="rangestep-function"></a><span data-ttu-id="f0cf8-102">Rangestep-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0cf8-102">RangeStep function</span></span>

<span data-ttu-id="f0cf8-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="f0cf8-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="f0cf8-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f0cf8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f0cf8-105">Gibt die ganze Zahl zurück, die angibt, wie der nächste Wert eines Bereichs berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="f0cf8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f0cf8-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="f0cf8-107">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="f0cf8-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="f0cf8-108">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f0cf8-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f0cf8-109">Der definierte Schrittwert des angegebenen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0cf8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0cf8-110">Remarks</span></span>

<span data-ttu-id="f0cf8-111">Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>