---
uid: Microsoft.Quantum.Core.RangeEnd
title: RangeEnd-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 90a9e31bf5c4a5e92a35998ddaec8c9e9de9888e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224036"
---
# <a name="rangeend-function"></a><span data-ttu-id="a4a40-102">RangeEnd-Funktion</span><span class="sxs-lookup"><span data-stu-id="a4a40-102">RangeEnd function</span></span>

<span data-ttu-id="a4a40-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="a4a40-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="a4a40-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a4a40-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a4a40-105">Gibt den definierten Endwert des angegebenen Bereichs zurück, der nicht notwendigerweise das letzte Element in der Sequenz ist.</span><span class="sxs-lookup"><span data-stu-id="a4a40-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="a4a40-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a4a40-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="a4a40-107">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="a4a40-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="a4a40-108">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a4a40-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a4a40-109">Der definierte Endwert des angegebenen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a4a40-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4a40-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4a40-110">Remarks</span></span>

<span data-ttu-id="a4a40-111">Das erste Element eines Bereichs Ausdrucks ist `start` , sein zweites Element `start+step` , das dritte Element ist `start+step+step` usw., bis erfolgreich `end` ist.</span><span class="sxs-lookup"><span data-stu-id="a4a40-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="a4a40-112">Beachten Sie, dass sich der definierte Endwert eines Bereichs von dem letzten Element in der Sequenz unterscheiden kann, die durch den Bereich angegeben wird. beispielsweise in einem Bereich von 0.</span><span class="sxs-lookup"><span data-stu-id="a4a40-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="a4a40-113">2..</span><span class="sxs-lookup"><span data-stu-id="a4a40-113">2 ..</span></span> <span data-ttu-id="a4a40-114">5 das letzte Element ist 4, der Endwert ist jedoch 5.</span><span class="sxs-lookup"><span data-stu-id="a4a40-114">5 the last element is 4 but the end value is 5.</span></span>