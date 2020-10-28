---
uid: Microsoft.Quantum.Arrays.Excluding
title: Ausschluss Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 8848c6e89da50efb4f7550168f1757b25a214a24
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706047"
---
# <a name="excluding-function"></a><span data-ttu-id="87026-102">Ausschluss Funktion</span><span class="sxs-lookup"><span data-stu-id="87026-102">Excluding function</span></span>

<span data-ttu-id="87026-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="87026-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="87026-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="87026-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="87026-105">Gibt ein Array mit den Elementen eines anderen Arrays zurück, wobei Elemente in einer angegebenen Liste von Indizes ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="87026-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="87026-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="87026-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="87026-107">Remove: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="87026-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="87026-108">Ein Array von Indizes, das festlegt, welche Elemente aus der Ausgabe ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="87026-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="87026-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="87026-109">array : 'T[]</span></span>

<span data-ttu-id="87026-110">Ein Array, dessen Werte im Ausgabe Array entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="87026-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="87026-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="87026-111">Output : 'T[]</span></span>

<span data-ttu-id="87026-112">Ein Array, `output` das `output[0]` das erste Element von ist, `array` dessen Index nicht in angezeigt wird `remove` , z `output[1]` . b. das zweite Element dieser Art usw.</span><span class="sxs-lookup"><span data-stu-id="87026-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="87026-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="87026-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="87026-114">GIF</span><span class="sxs-lookup"><span data-stu-id="87026-114">'T</span></span>

<span data-ttu-id="87026-115">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="87026-115">The type of the array elements.</span></span>