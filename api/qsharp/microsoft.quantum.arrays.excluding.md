---
uid: Microsoft.Quantum.Arrays.Excluding
title: Ausschluss Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 6585e619834a96953c9eae2d36a8ebe0a11dbda0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221316"
---
# <a name="excluding-function"></a><span data-ttu-id="84e2b-102">Ausschluss Funktion</span><span class="sxs-lookup"><span data-stu-id="84e2b-102">Excluding function</span></span>

<span data-ttu-id="84e2b-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="84e2b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="84e2b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="84e2b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="84e2b-105">Gibt ein Array mit den Elementen eines anderen Arrays zurück, wobei Elemente in einer angegebenen Liste von Indizes ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="84e2b-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="84e2b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84e2b-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="84e2b-107">Remove: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="84e2b-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="84e2b-108">Ein Array von Indizes, das festlegt, welche Elemente aus der Ausgabe ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="84e2b-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="84e2b-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="84e2b-109">array : 'T[]</span></span>

<span data-ttu-id="84e2b-110">Ein Array, dessen Werte im Ausgabe Array entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="84e2b-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="84e2b-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="84e2b-111">Output : 'T[]</span></span>

<span data-ttu-id="84e2b-112">Ein Array, `output` das `output[0]` das erste Element von ist, `array` dessen Index nicht in angezeigt wird `remove` , z `output[1]` . b. das zweite Element dieser Art usw.</span><span class="sxs-lookup"><span data-stu-id="84e2b-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="84e2b-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="84e2b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="84e2b-114">GIF</span><span class="sxs-lookup"><span data-stu-id="84e2b-114">'T</span></span>

<span data-ttu-id="84e2b-115">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="84e2b-115">The type of the array elements.</span></span>