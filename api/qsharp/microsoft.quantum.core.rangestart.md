---
uid: Microsoft.Quantum.Core.RangeStart
title: RangeStart-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 3e4b0cebe34b4c98cb1d582a9cd11b46ff778517
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702839"
---
# <a name="rangestart-function"></a><span data-ttu-id="1904d-102">RangeStart-Funktion</span><span class="sxs-lookup"><span data-stu-id="1904d-102">RangeStart function</span></span>

<span data-ttu-id="1904d-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="1904d-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="1904d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1904d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1904d-105">Gibt den definierten Startwert des angegebenen Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="1904d-105">Returns the defined start value of the given range.</span></span>

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="1904d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1904d-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="1904d-107">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="1904d-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="1904d-108">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1904d-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1904d-109">Der definierte Startwert des angegebenen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="1904d-109">The defined start value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="1904d-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1904d-110">Remarks</span></span>

<span data-ttu-id="1904d-111">Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.</span><span class="sxs-lookup"><span data-stu-id="1904d-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="1904d-112">Beachten Sie, dass der definierte Startwert eines Bereichs mit dem ersten Element der Sequenz übereinstimmt, es sei denn, der Bereich gibt eine leere Sequenz an (z. b. 2.).</span><span class="sxs-lookup"><span data-stu-id="1904d-112">Note that the defined start value of a range is the same as the first element of the sequence, unless the range specifies an empty sequence (for example, 2 ..</span></span> <span data-ttu-id="1904d-113">1).</span><span class="sxs-lookup"><span data-stu-id="1904d-113">1).</span></span>