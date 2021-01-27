---
uid: Microsoft.Quantum.Arrays.Zip4
title: Zip4-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip4
qsharp.summary: >-
  > [!WARNING]

  > Zip4 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.


  Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: 534721e6544a31f6f5d27db0c077e9d8c574aecd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850880"
---
# <a name="zip4-function"></a><span data-ttu-id="28053-102">Zip4-Funktion</span><span class="sxs-lookup"><span data-stu-id="28053-102">Zip4 function</span></span>

<span data-ttu-id="28053-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="28053-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="28053-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="28053-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="28053-105">Zip4 wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="28053-105">Zip4 has been deprecated.</span></span> <span data-ttu-id="28053-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Arrays.Zipped4>.</span><span class="sxs-lookup"><span data-stu-id="28053-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.</span></span>

<span data-ttu-id="28053-107">Bei Angabe von vier Arrays wird ein neues Array von 4-Tupeln zurückgegeben, sodass jedes 4-Tupel ein Element aus jedem ursprünglichen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="28053-107">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zip4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="28053-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28053-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="28053-109">zuerst: 't 1 []</span><span class="sxs-lookup"><span data-stu-id="28053-109">first : 'T1[]</span></span>

<span data-ttu-id="28053-110">Ein Array, das Werte für das erste Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="28053-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="28053-111">Zweitens: 't 2 []</span><span class="sxs-lookup"><span data-stu-id="28053-111">second : 'T2[]</span></span>

<span data-ttu-id="28053-112">Ein Array, das Werte für das zweite Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="28053-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="28053-113">Drittens: 't 3 []</span><span class="sxs-lookup"><span data-stu-id="28053-113">third : 'T3[]</span></span>

<span data-ttu-id="28053-114">Ein Array, das Werte für das dritte Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="28053-114">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="28053-115">Fourth: 't 4 []</span><span class="sxs-lookup"><span data-stu-id="28053-115">fourth : 'T4[]</span></span>

<span data-ttu-id="28053-116">Ein Array, das Werte für das vierte Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="28053-116">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="28053-117">Ausgabe: ('t 1, 't 2, 't 3, 't 4) []</span><span class="sxs-lookup"><span data-stu-id="28053-117">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="28053-118">Ein Array, das 4 Tupel des Formulars `(first[idx], second[idx], third[idx], fourth[idx])` für jedes enthält `idx` .</span><span class="sxs-lookup"><span data-stu-id="28053-118">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="28053-119">Wenn die vier Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.</span><span class="sxs-lookup"><span data-stu-id="28053-119">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="28053-120">Typparameter</span><span class="sxs-lookup"><span data-stu-id="28053-120">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="28053-121">Nicht 1</span><span class="sxs-lookup"><span data-stu-id="28053-121">'T1</span></span>

<span data-ttu-id="28053-122">Der Typ der ersten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="28053-122">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="28053-123">Nicht 2</span><span class="sxs-lookup"><span data-stu-id="28053-123">'T2</span></span>

<span data-ttu-id="28053-124">Der Typ der zweiten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="28053-124">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="28053-125">Nicht 3</span><span class="sxs-lookup"><span data-stu-id="28053-125">'T3</span></span>

<span data-ttu-id="28053-126">Der Typ der dritten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="28053-126">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="28053-127">'T 4</span><span class="sxs-lookup"><span data-stu-id="28053-127">'T4</span></span>

<span data-ttu-id="28053-128">Der Typ der vierten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="28053-128">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="28053-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="28053-129">See Also</span></span>

- [<span data-ttu-id="28053-130">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="28053-130">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="28053-131">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="28053-131">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)