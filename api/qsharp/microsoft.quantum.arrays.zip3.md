---
uid: Microsoft.Quantum.Arrays.Zip3
title: Zip3-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip3
qsharp.summary: >-
  > [!WARNING]

  > Zip3 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.


  Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: b41b0789cdf90db534ee7a50ff25eb3a931ec683
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845352"
---
# <a name="zip3-function"></a><span data-ttu-id="7d8d6-102">Zip3-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d8d6-102">Zip3 function</span></span>

<span data-ttu-id="7d8d6-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7d8d6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7d8d6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7d8d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="7d8d6-105">Zip3 wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-105">Zip3 has been deprecated.</span></span> <span data-ttu-id="7d8d6-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Arrays.Zipped3>.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.</span></span>

<span data-ttu-id="7d8d6-107">Bei drei Arrays gibt ein neues Array von 3-Tupeln zurück, sodass jedes 3-Tupel ein Element aus jedem ursprünglichen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-107">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zip3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="7d8d6-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7d8d6-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="7d8d6-109">zuerst: 't 1 []</span><span class="sxs-lookup"><span data-stu-id="7d8d6-109">first : 'T1[]</span></span>

<span data-ttu-id="7d8d6-110">Ein Array, das Werte für das erste Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="7d8d6-111">Zweitens: 't 2 []</span><span class="sxs-lookup"><span data-stu-id="7d8d6-111">second : 'T2[]</span></span>

<span data-ttu-id="7d8d6-112">Ein Array, das Werte für das zweite Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="7d8d6-113">Drittens: 't 3 []</span><span class="sxs-lookup"><span data-stu-id="7d8d6-113">third : 'T3[]</span></span>

<span data-ttu-id="7d8d6-114">Ein Array, das Werte für das dritte Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-114">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="7d8d6-115">Ausgabe: ('t 1, 't 2, 't 3) []</span><span class="sxs-lookup"><span data-stu-id="7d8d6-115">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="7d8d6-116">Ein Array, das jeweils 3 Tupel des Formulars enthält `(first[idx], second[idx], third[idx])` `idx` .</span><span class="sxs-lookup"><span data-stu-id="7d8d6-116">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="7d8d6-117">Wenn die drei Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-117">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7d8d6-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7d8d6-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="7d8d6-119">Nicht 1</span><span class="sxs-lookup"><span data-stu-id="7d8d6-119">'T1</span></span>

<span data-ttu-id="7d8d6-120">Der Typ der ersten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="7d8d6-121">Nicht 2</span><span class="sxs-lookup"><span data-stu-id="7d8d6-121">'T2</span></span>

<span data-ttu-id="7d8d6-122">Der Typ der zweiten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="7d8d6-123">Nicht 3</span><span class="sxs-lookup"><span data-stu-id="7d8d6-123">'T3</span></span>

<span data-ttu-id="7d8d6-124">Der Typ der dritten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-124">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d8d6-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7d8d6-125">See Also</span></span>

- [<span data-ttu-id="7d8d6-126">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="7d8d6-126">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="7d8d6-127">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="7d8d6-127">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)