---
uid: Microsoft.Quantum.Arrays.Exclude
title: Exclude-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: e1fa7e728d4846db90872055454a8182a77a518b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706050"
---
# <a name="exclude-function"></a><span data-ttu-id="72a3e-102">Exclude-Funktion</span><span class="sxs-lookup"><span data-stu-id="72a3e-102">Exclude function</span></span>

<span data-ttu-id="72a3e-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="72a3e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="72a3e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="72a3e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="72a3e-105">Gibt ein Array mit den Elementen eines anderen Arrays zurück, wobei Elemente in einer angegebenen Liste von Indizes ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="72a3e-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="72a3e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72a3e-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="72a3e-107">Remove: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="72a3e-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="72a3e-108">Ein Array von Indizes, das festlegt, welche Elemente aus der Ausgabe ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="72a3e-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="72a3e-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="72a3e-109">array : 'T[]</span></span>

<span data-ttu-id="72a3e-110">Ein Array, dessen Werte im Ausgabe Array entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="72a3e-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="72a3e-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="72a3e-111">Output : 'T[]</span></span>

<span data-ttu-id="72a3e-112">Ein Array, `output` das `output[0]` das erste Element von ist, `array` dessen Index nicht in angezeigt wird `remove` , z `output[1]` . b. das zweite Element dieser Art usw.</span><span class="sxs-lookup"><span data-stu-id="72a3e-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="72a3e-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="72a3e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="72a3e-114">GIF</span><span class="sxs-lookup"><span data-stu-id="72a3e-114">'T</span></span>

<span data-ttu-id="72a3e-115">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="72a3e-115">The type of the array elements.</span></span>