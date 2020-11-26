---
uid: Microsoft.Quantum.Arrays.Zipped3
title: Zipped3-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: 37fda4082a46870270414649f807659fa561962b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219684"
---
# <a name="zipped3-function"></a><span data-ttu-id="66249-102">Zipped3-Funktion</span><span class="sxs-lookup"><span data-stu-id="66249-102">Zipped3 function</span></span>

<span data-ttu-id="66249-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="66249-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="66249-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66249-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66249-105">Bei drei Arrays gibt ein neues Array von 3-Tupeln zurück, sodass jedes 3-Tupel ein Element aus jedem ursprünglichen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="66249-105">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="66249-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="66249-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="66249-107">zuerst: 't 1 []</span><span class="sxs-lookup"><span data-stu-id="66249-107">first : 'T1[]</span></span>

<span data-ttu-id="66249-108">Ein Array, das Werte für das erste Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="66249-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="66249-109">Zweitens: 't 2 []</span><span class="sxs-lookup"><span data-stu-id="66249-109">second : 'T2[]</span></span>

<span data-ttu-id="66249-110">Ein Array, das Werte für das zweite Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="66249-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="66249-111">Drittens: 't 3 []</span><span class="sxs-lookup"><span data-stu-id="66249-111">third : 'T3[]</span></span>

<span data-ttu-id="66249-112">Ein Array, das Werte für das dritte Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="66249-112">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="66249-113">Ausgabe: ('t 1, 't 2, 't 3) []</span><span class="sxs-lookup"><span data-stu-id="66249-113">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="66249-114">Ein Array, das jeweils 3 Tupel des Formulars enthält `(first[idx], second[idx], third[idx])` `idx` .</span><span class="sxs-lookup"><span data-stu-id="66249-114">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="66249-115">Wenn die drei Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.</span><span class="sxs-lookup"><span data-stu-id="66249-115">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="66249-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="66249-116">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="66249-117">Nicht 1</span><span class="sxs-lookup"><span data-stu-id="66249-117">'T1</span></span>

<span data-ttu-id="66249-118">Der Typ der ersten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="66249-118">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="66249-119">Nicht 2</span><span class="sxs-lookup"><span data-stu-id="66249-119">'T2</span></span>

<span data-ttu-id="66249-120">Der Typ der zweiten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="66249-120">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="66249-121">Nicht 3</span><span class="sxs-lookup"><span data-stu-id="66249-121">'T3</span></span>

<span data-ttu-id="66249-122">Der Typ der dritten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="66249-122">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="66249-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="66249-123">See Also</span></span>

- [<span data-ttu-id="66249-124">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="66249-124">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="66249-125">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="66249-125">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)