---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Squarearrayfact-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: 3529718f0c903266d21fd593c11c0149dae0fa2c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220194"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="cc894-102">Squarearrayfact-Funktion</span><span class="sxs-lookup"><span data-stu-id="cc894-102">SquareArrayFact function</span></span>

<span data-ttu-id="cc894-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="cc894-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="cc894-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc894-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cc894-105">Stellt eine Bedingung dar, dass ein zweidimensionales Array über eine quadratische Form verfügt.</span><span class="sxs-lookup"><span data-stu-id="cc894-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="cc894-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc894-106">Description</span></span>

<span data-ttu-id="cc894-107">Diese Funktion bestätigt, dass jede Zeile in einem Array so viele Elemente aufweist, wie Zeilen (Elemente) im Array vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cc894-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="cc894-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc894-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="cc894-109">Array: 't [] []</span><span class="sxs-lookup"><span data-stu-id="cc894-109">array : 'T[][]</span></span>

<span data-ttu-id="cc894-110">Ein zweidimensionales Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="cc894-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="cc894-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="cc894-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="cc894-112">Eine Meldung, die gedruckt werden soll, wenn das Array kein quadratisches Array ist</span><span class="sxs-lookup"><span data-stu-id="cc894-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="cc894-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cc894-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cc894-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="cc894-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cc894-115">GIF</span><span class="sxs-lookup"><span data-stu-id="cc894-115">'T</span></span>

<span data-ttu-id="cc894-116">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="cc894-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc894-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cc894-117">See Also</span></span>

- [<span data-ttu-id="cc894-118">Microsoft. Quantum. Arrays. rechgulararrayfact</span><span class="sxs-lookup"><span data-stu-id="cc894-118">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)