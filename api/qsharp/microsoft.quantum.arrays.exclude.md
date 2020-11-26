---
uid: Microsoft.Quantum.Arrays.Exclude
title: Exclude-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 4ea0d754fce4fc7e3e4e42e55b56720cb3f95ca6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221350"
---
# <a name="exclude-function"></a><span data-ttu-id="d4545-102">Exclude-Funktion</span><span class="sxs-lookup"><span data-stu-id="d4545-102">Exclude function</span></span>

<span data-ttu-id="d4545-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d4545-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d4545-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d4545-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d4545-105">Gibt ein Array mit den Elementen eines anderen Arrays zurück, wobei Elemente in einer angegebenen Liste von Indizes ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d4545-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="d4545-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4545-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="d4545-107">Remove: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d4545-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d4545-108">Ein Array von Indizes, das festlegt, welche Elemente aus der Ausgabe ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4545-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="d4545-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="d4545-109">array : 'T[]</span></span>

<span data-ttu-id="d4545-110">Ein Array, dessen Werte im Ausgabe Array entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="d4545-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="d4545-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="d4545-111">Output : 'T[]</span></span>

<span data-ttu-id="d4545-112">Ein Array, `output` das `output[0]` das erste Element von ist, `array` dessen Index nicht in angezeigt wird `remove` , z `output[1]` . b. das zweite Element dieser Art usw.</span><span class="sxs-lookup"><span data-stu-id="d4545-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d4545-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d4545-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d4545-114">GIF</span><span class="sxs-lookup"><span data-stu-id="d4545-114">'T</span></span>

<span data-ttu-id="d4545-115">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="d4545-115">The type of the array elements.</span></span>