---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Squarearrayfact-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: f7f0573db9098feebfd481624e11119c58fd9eed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705767"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="c798e-102">Squarearrayfact-Funktion</span><span class="sxs-lookup"><span data-stu-id="c798e-102">SquareArrayFact function</span></span>

<span data-ttu-id="c798e-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c798e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c798e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c798e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c798e-105">Stellt eine Bedingung dar, dass ein zweidimensionales Array über eine quadratische Form verfügt.</span><span class="sxs-lookup"><span data-stu-id="c798e-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="c798e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c798e-106">Description</span></span>

<span data-ttu-id="c798e-107">Diese Funktion bestätigt, dass jede Zeile in einem Array so viele Elemente aufweist, wie Zeilen (Elemente) im Array vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c798e-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="c798e-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c798e-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="c798e-109">Array: 't [] []</span><span class="sxs-lookup"><span data-stu-id="c798e-109">array : 'T[][]</span></span>

<span data-ttu-id="c798e-110">Ein zweidimensionales Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="c798e-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="c798e-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c798e-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c798e-112">Eine Meldung, die gedruckt werden soll, wenn das Array kein quadratisches Array ist</span><span class="sxs-lookup"><span data-stu-id="c798e-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="c798e-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c798e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c798e-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c798e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c798e-115">GIF</span><span class="sxs-lookup"><span data-stu-id="c798e-115">'T</span></span>

<span data-ttu-id="c798e-116">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="c798e-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="c798e-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c798e-117">See Also</span></span>

- [<span data-ttu-id="c798e-118">Microsoft. Quantum. Arrays. rechgulararrayfact</span><span class="sxs-lookup"><span data-stu-id="c798e-118">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)