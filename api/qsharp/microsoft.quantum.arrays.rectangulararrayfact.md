---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Rechgulararrayfact-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: 8cf6b85da6e8fee7fc255a173753a6468d8134b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845487"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="4e606-102">Rechgulararrayfact-Funktion</span><span class="sxs-lookup"><span data-stu-id="4e606-102">RectangularArrayFact function</span></span>

<span data-ttu-id="4e606-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4e606-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4e606-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4e606-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4e606-105">Stellt eine Bedingung dar, dass ein zweidimensionales Array eine rechteckige Form aufweist.</span><span class="sxs-lookup"><span data-stu-id="4e606-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="4e606-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e606-106">Description</span></span>

<span data-ttu-id="4e606-107">Diese Funktion bestätigt, dass jede Zeile in einem Array die gleiche Länge aufweist.</span><span class="sxs-lookup"><span data-stu-id="4e606-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="4e606-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4e606-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="4e606-109">Array: 't [] []</span><span class="sxs-lookup"><span data-stu-id="4e606-109">array : 'T[][]</span></span>

<span data-ttu-id="4e606-110">Ein zweidimensionales Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="4e606-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="4e606-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="4e606-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="4e606-112">Eine Meldung, die gedruckt werden soll, wenn das Array kein rechteckiges Array ist</span><span class="sxs-lookup"><span data-stu-id="4e606-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="4e606-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4e606-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4e606-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="4e606-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4e606-115">GIF</span><span class="sxs-lookup"><span data-stu-id="4e606-115">'T</span></span>

<span data-ttu-id="4e606-116">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="4e606-116">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="4e606-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4e606-117">Example</span></span>

```qsharp
RectangularArrayFact([[1, 2], [3, 4]], "Array is not rectangular");       // okay
RectangularArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not rectangular"); // okay
RectangularArrayFact([[1, 2], [3, 4, 5]], "Array is not rectangular");    // will fail
```

## <a name="see-also"></a><span data-ttu-id="4e606-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4e606-118">See Also</span></span>

- [<span data-ttu-id="4e606-119">Microsoft. Quantum. Arrays. squarearrayfact</span><span class="sxs-lookup"><span data-stu-id="4e606-119">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)