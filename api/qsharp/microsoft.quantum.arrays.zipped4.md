---
uid: Microsoft.Quantum.Arrays.Zipped4
title: Zipped4-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped4
qsharp.summary: Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: d5ee10ac9776383e75bc16a5c003a8b1a65c5698
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219633"
---
# <a name="zipped4-function"></a><span data-ttu-id="dd13e-102">Zipped4-Funktion</span><span class="sxs-lookup"><span data-stu-id="dd13e-102">Zipped4 function</span></span>

<span data-ttu-id="dd13e-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dd13e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dd13e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dd13e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dd13e-105">Bei Angabe von vier Arrays wird ein neues Array von 4-Tupeln zurückgegeben, sodass jedes 4-Tupel ein Element aus jedem ursprünglichen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="dd13e-105">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="dd13e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dd13e-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="dd13e-107">zuerst: 't 1 []</span><span class="sxs-lookup"><span data-stu-id="dd13e-107">first : 'T1[]</span></span>

<span data-ttu-id="dd13e-108">Ein Array, das Werte für das erste Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="dd13e-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="dd13e-109">Zweitens: 't 2 []</span><span class="sxs-lookup"><span data-stu-id="dd13e-109">second : 'T2[]</span></span>

<span data-ttu-id="dd13e-110">Ein Array, das Werte für das zweite Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="dd13e-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="dd13e-111">Drittens: 't 3 []</span><span class="sxs-lookup"><span data-stu-id="dd13e-111">third : 'T3[]</span></span>

<span data-ttu-id="dd13e-112">Ein Array, das Werte für das dritte Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="dd13e-112">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="dd13e-113">Fourth: 't 4 []</span><span class="sxs-lookup"><span data-stu-id="dd13e-113">fourth : 'T4[]</span></span>

<span data-ttu-id="dd13e-114">Ein Array, das Werte für das vierte Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="dd13e-114">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="dd13e-115">Ausgabe: ('t 1, 't 2, 't 3, 't 4) []</span><span class="sxs-lookup"><span data-stu-id="dd13e-115">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="dd13e-116">Ein Array, das 4 Tupel des Formulars `(first[idx], second[idx], third[idx], fourth[idx])` für jedes enthält `idx` .</span><span class="sxs-lookup"><span data-stu-id="dd13e-116">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="dd13e-117">Wenn die vier Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.</span><span class="sxs-lookup"><span data-stu-id="dd13e-117">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dd13e-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="dd13e-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="dd13e-119">Nicht 1</span><span class="sxs-lookup"><span data-stu-id="dd13e-119">'T1</span></span>

<span data-ttu-id="dd13e-120">Der Typ der ersten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="dd13e-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="dd13e-121">Nicht 2</span><span class="sxs-lookup"><span data-stu-id="dd13e-121">'T2</span></span>

<span data-ttu-id="dd13e-122">Der Typ der zweiten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="dd13e-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="dd13e-123">Nicht 3</span><span class="sxs-lookup"><span data-stu-id="dd13e-123">'T3</span></span>

<span data-ttu-id="dd13e-124">Der Typ der dritten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="dd13e-124">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="dd13e-125">'T 4</span><span class="sxs-lookup"><span data-stu-id="dd13e-125">'T4</span></span>

<span data-ttu-id="dd13e-126">Der Typ der vierten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="dd13e-126">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd13e-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dd13e-127">See Also</span></span>

- [<span data-ttu-id="dd13e-128">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="dd13e-128">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="dd13e-129">Microsoft.Quantum.Arrays.ZipPED3</span><span class="sxs-lookup"><span data-stu-id="dd13e-129">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)