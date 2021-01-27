---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Squarearrayfact-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: a154e5becba4dae762596a3fc1b268855520fa1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850963"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="bf53e-102">Squarearrayfact-Funktion</span><span class="sxs-lookup"><span data-stu-id="bf53e-102">SquareArrayFact function</span></span>

<span data-ttu-id="bf53e-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bf53e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bf53e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bf53e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bf53e-105">Stellt eine Bedingung dar, dass ein zweidimensionales Array über eine quadratische Form verfügt.</span><span class="sxs-lookup"><span data-stu-id="bf53e-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="bf53e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf53e-106">Description</span></span>

<span data-ttu-id="bf53e-107">Diese Funktion bestätigt, dass jede Zeile in einem Array so viele Elemente aufweist, wie Zeilen (Elemente) im Array vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bf53e-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="bf53e-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bf53e-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="bf53e-109">Array: 't [] []</span><span class="sxs-lookup"><span data-stu-id="bf53e-109">array : 'T[][]</span></span>

<span data-ttu-id="bf53e-110">Ein zweidimensionales Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="bf53e-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="bf53e-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="bf53e-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="bf53e-112">Eine Meldung, die gedruckt werden soll, wenn das Array kein quadratisches Array ist</span><span class="sxs-lookup"><span data-stu-id="bf53e-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="bf53e-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bf53e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bf53e-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="bf53e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bf53e-115">GIF</span><span class="sxs-lookup"><span data-stu-id="bf53e-115">'T</span></span>

<span data-ttu-id="bf53e-116">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="bf53e-116">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="bf53e-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bf53e-117">Example</span></span>

```qsharp
SquareArrayFact([[1, 2], [3, 4]], "Array is not a square");       // okay
SquareArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not a square"); // will fail
SquareArrayFact([[1, 2], [3, 4, 5]], "Array is not a square");    // will fail
```

## <a name="see-also"></a><span data-ttu-id="bf53e-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bf53e-118">See Also</span></span>

- [<span data-ttu-id="bf53e-119">Microsoft. Quantum. Arrays. rechgulararrayfact</span><span class="sxs-lookup"><span data-stu-id="bf53e-119">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)