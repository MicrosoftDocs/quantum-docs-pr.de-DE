---
uid: Microsoft.Quantum.Core.RangeStep
title: Rangestep-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: 667b579337eec28d6b75de61668bd79de176883e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853598"
---
# <a name="rangestep-function"></a><span data-ttu-id="80ed8-102">Rangestep-Funktion</span><span class="sxs-lookup"><span data-stu-id="80ed8-102">RangeStep function</span></span>

<span data-ttu-id="80ed8-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="80ed8-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="80ed8-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="80ed8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="80ed8-105">Gibt die ganze Zahl zurück, die angibt, wie der nächste Wert eines Bereichs berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="80ed8-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="80ed8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80ed8-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="80ed8-107">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="80ed8-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="80ed8-108">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="80ed8-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="80ed8-109">Der definierte Schrittwert des angegebenen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="80ed8-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="80ed8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80ed8-110">Remarks</span></span>

<span data-ttu-id="80ed8-111">Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.</span><span class="sxs-lookup"><span data-stu-id="80ed8-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>