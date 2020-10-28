---
uid: Microsoft.Quantum.Arrays.Zip
title: ZIP-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 32fea60fc36bfdbaa2ab2f3560f291bf4ce4fa51
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705682"
---
# <a name="zip-function"></a><span data-ttu-id="8aec0-102">ZIP-Funktion</span><span class="sxs-lookup"><span data-stu-id="8aec0-102">Zip function</span></span>

<span data-ttu-id="8aec0-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8aec0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8aec0-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8aec0-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="8aec0-105">ZIP ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="8aec0-105">Zip has been deprecated.</span></span> <span data-ttu-id="8aec0-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Arrays.Zipped>.</span><span class="sxs-lookup"><span data-stu-id="8aec0-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="8aec0-107">Bei zwei Arrays wird ein neues Array von Paaren zurückgegeben, sodass jedes Paar ein Element aus jedem ursprünglichen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="8aec0-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="8aec0-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8aec0-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="8aec0-109">Left: 't []</span><span class="sxs-lookup"><span data-stu-id="8aec0-109">left : 'T[]</span></span>

<span data-ttu-id="8aec0-110">Ein Array, das Werte für das erste Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="8aec0-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="8aec0-111">Right: ' U []</span><span class="sxs-lookup"><span data-stu-id="8aec0-111">right : 'U[]</span></span>

<span data-ttu-id="8aec0-112">Ein Array, das Werte für das zweite Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="8aec0-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="8aec0-113">Ausgabe: ('t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="8aec0-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="8aec0-114">Ein Array, das Paare des Formulars `(left[idx], right[idx])` für jedes enthält `idx` .</span><span class="sxs-lookup"><span data-stu-id="8aec0-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="8aec0-115">Wenn die beiden Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8aec0-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8aec0-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8aec0-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8aec0-117">GIF</span><span class="sxs-lookup"><span data-stu-id="8aec0-117">'T</span></span>

<span data-ttu-id="8aec0-118">Der Typ der linken Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="8aec0-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="8aec0-119">"U</span><span class="sxs-lookup"><span data-stu-id="8aec0-119">'U</span></span>

<span data-ttu-id="8aec0-120">Der Typ der rechten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="8aec0-120">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="8aec0-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8aec0-121">See Also</span></span>

- [<span data-ttu-id="8aec0-122">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="8aec0-122">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="8aec0-123">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="8aec0-123">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="8aec0-124">Microsoft. Quantum. Arrays. entzippt</span><span class="sxs-lookup"><span data-stu-id="8aec0-124">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)