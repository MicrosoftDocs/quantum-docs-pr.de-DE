---
uid: Microsoft.Quantum.Arrays.Zipped4
title: Zipped4-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped4
qsharp.summary: Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: 413b415288170b4a6bffbb773e3277cdb47bdbbe
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705650"
---
# <a name="zipped4-function"></a><span data-ttu-id="7cc8c-102">Zipped4-Funktion</span><span class="sxs-lookup"><span data-stu-id="7cc8c-102">Zipped4 function</span></span>

<span data-ttu-id="7cc8c-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7cc8c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7cc8c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7cc8c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7cc8c-105">Bei Angabe von vier Arrays wird ein neues Array von 4-Tupeln zurückgegeben, sodass jedes 4-Tupel ein Element aus jedem ursprünglichen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-105">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="7cc8c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7cc8c-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="7cc8c-107">zuerst: 't 1 []</span><span class="sxs-lookup"><span data-stu-id="7cc8c-107">first : 'T1[]</span></span>

<span data-ttu-id="7cc8c-108">Ein Array, das Werte für das erste Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="7cc8c-109">Zweitens: 't 2 []</span><span class="sxs-lookup"><span data-stu-id="7cc8c-109">second : 'T2[]</span></span>

<span data-ttu-id="7cc8c-110">Ein Array, das Werte für das zweite Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="7cc8c-111">Drittens: 't 3 []</span><span class="sxs-lookup"><span data-stu-id="7cc8c-111">third : 'T3[]</span></span>

<span data-ttu-id="7cc8c-112">Ein Array, das Werte für das dritte Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-112">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="7cc8c-113">Fourth: 't 4 []</span><span class="sxs-lookup"><span data-stu-id="7cc8c-113">fourth : 'T4[]</span></span>

<span data-ttu-id="7cc8c-114">Ein Array, das Werte für das vierte Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-114">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="7cc8c-115">Ausgabe: ('t 1, 't 2, 't 3, 't 4) []</span><span class="sxs-lookup"><span data-stu-id="7cc8c-115">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="7cc8c-116">Ein Array, das 4 Tupel des Formulars `(first[idx], second[idx], third[idx], fourth[idx])` für jedes enthält `idx` .</span><span class="sxs-lookup"><span data-stu-id="7cc8c-116">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="7cc8c-117">Wenn die vier Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-117">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7cc8c-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7cc8c-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="7cc8c-119">Nicht 1</span><span class="sxs-lookup"><span data-stu-id="7cc8c-119">'T1</span></span>

<span data-ttu-id="7cc8c-120">Der Typ der ersten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="7cc8c-121">Nicht 2</span><span class="sxs-lookup"><span data-stu-id="7cc8c-121">'T2</span></span>

<span data-ttu-id="7cc8c-122">Der Typ der zweiten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="7cc8c-123">Nicht 3</span><span class="sxs-lookup"><span data-stu-id="7cc8c-123">'T3</span></span>

<span data-ttu-id="7cc8c-124">Der Typ der dritten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-124">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="7cc8c-125">'T 4</span><span class="sxs-lookup"><span data-stu-id="7cc8c-125">'T4</span></span>

<span data-ttu-id="7cc8c-126">Der Typ der vierten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="7cc8c-126">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cc8c-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7cc8c-127">See Also</span></span>

- [<span data-ttu-id="7cc8c-128">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="7cc8c-128">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="7cc8c-129">Microsoft.Quantum.Arrays.ZipPED3</span><span class="sxs-lookup"><span data-stu-id="7cc8c-129">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)