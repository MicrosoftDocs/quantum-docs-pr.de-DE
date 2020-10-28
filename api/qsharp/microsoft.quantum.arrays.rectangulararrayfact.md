---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Rechgulararrayfact-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: f0d3f4d6bfa9e86f1c7a91792c09e16fe86433a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705810"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="c75dc-102">Rechgulararrayfact-Funktion</span><span class="sxs-lookup"><span data-stu-id="c75dc-102">RectangularArrayFact function</span></span>

<span data-ttu-id="c75dc-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c75dc-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c75dc-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c75dc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c75dc-105">Stellt eine Bedingung dar, dass ein zweidimensionales Array eine rechteckige Form aufweist.</span><span class="sxs-lookup"><span data-stu-id="c75dc-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="c75dc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c75dc-106">Description</span></span>

<span data-ttu-id="c75dc-107">Diese Funktion bestätigt, dass jede Zeile in einem Array die gleiche Länge aufweist.</span><span class="sxs-lookup"><span data-stu-id="c75dc-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="c75dc-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c75dc-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="c75dc-109">Array: 't [] []</span><span class="sxs-lookup"><span data-stu-id="c75dc-109">array : 'T[][]</span></span>

<span data-ttu-id="c75dc-110">Ein zweidimensionales Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="c75dc-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="c75dc-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c75dc-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c75dc-112">Eine Meldung, die gedruckt werden soll, wenn das Array kein rechteckiges Array ist</span><span class="sxs-lookup"><span data-stu-id="c75dc-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="c75dc-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c75dc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c75dc-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c75dc-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c75dc-115">GIF</span><span class="sxs-lookup"><span data-stu-id="c75dc-115">'T</span></span>

<span data-ttu-id="c75dc-116">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="c75dc-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="c75dc-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c75dc-117">See Also</span></span>

- [<span data-ttu-id="c75dc-118">Microsoft. Quantum. Arrays. squarearrayfact</span><span class="sxs-lookup"><span data-stu-id="c75dc-118">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)