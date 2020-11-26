---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Rechgulararrayfact-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: b8ef7d52f7f815ca3e21ded1236e775a381646cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220415"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="ee4ad-102">Rechgulararrayfact-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee4ad-102">RectangularArrayFact function</span></span>

<span data-ttu-id="ee4ad-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ee4ad-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ee4ad-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ee4ad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ee4ad-105">Stellt eine Bedingung dar, dass ein zweidimensionales Array eine rechteckige Form aufweist.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="ee4ad-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee4ad-106">Description</span></span>

<span data-ttu-id="ee4ad-107">Diese Funktion bestätigt, dass jede Zeile in einem Array die gleiche Länge aufweist.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="ee4ad-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ee4ad-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="ee4ad-109">Array: 't [] []</span><span class="sxs-lookup"><span data-stu-id="ee4ad-109">array : 'T[][]</span></span>

<span data-ttu-id="ee4ad-110">Ein zweidimensionales Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="ee4ad-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="ee4ad-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="ee4ad-112">Eine Meldung, die gedruckt werden soll, wenn das Array kein rechteckiges Array ist</span><span class="sxs-lookup"><span data-stu-id="ee4ad-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="ee4ad-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ee4ad-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ee4ad-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ee4ad-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ee4ad-115">GIF</span><span class="sxs-lookup"><span data-stu-id="ee4ad-115">'T</span></span>

<span data-ttu-id="ee4ad-116">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="ee4ad-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee4ad-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ee4ad-117">See Also</span></span>

- [<span data-ttu-id="ee4ad-118">Microsoft. Quantum. Arrays. squarearrayfact</span><span class="sxs-lookup"><span data-stu-id="ee4ad-118">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)