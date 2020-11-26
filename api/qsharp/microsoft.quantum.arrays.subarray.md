---
uid: Microsoft.Quantum.Arrays.Subarray
title: Subarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: cf72f04421b277ce64354d1eccec11cbc61d78cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220160"
---
# <a name="subarray-function"></a><span data-ttu-id="a68d6-102">Subarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="a68d6-102">Subarray function</span></span>

<span data-ttu-id="a68d6-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a68d6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a68d6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a68d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a68d6-105">Nimmt ein Array und eine Liste von Speicherorten an und erstellt ein neues Array, das aus den Elementen des ursprünglichen Arrays gebildet wird, die den angegebenen Speicherorten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a68d6-105">Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.</span></span>

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="a68d6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a68d6-106">Input</span></span>

### <a name="indices--int"></a><span data-ttu-id="a68d6-107">Indizes: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="a68d6-107">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="a68d6-108">Eine Liste von ganzen Zahlen, die zum Definieren des Unterarrays verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a68d6-108">A list of integers that is used to define the subarray.</span></span>


### <a name="array--t"></a><span data-ttu-id="a68d6-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="a68d6-109">array : 'T[]</span></span>

<span data-ttu-id="a68d6-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="a68d6-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="a68d6-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="a68d6-111">Output : 'T[]</span></span>

<span data-ttu-id="a68d6-112">Ein Array `out` von-Elementen, deren Indizes dem Unterarray entsprechen, z `out[idx] == array[indices[idx]]` . b..</span><span class="sxs-lookup"><span data-stu-id="a68d6-112">An array `out` of elements whose indices correspond to the subarray, such that `out[idx] == array[indices[idx]]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a68d6-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a68d6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a68d6-114">GIF</span><span class="sxs-lookup"><span data-stu-id="a68d6-114">'T</span></span>

<span data-ttu-id="a68d6-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="a68d6-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="a68d6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a68d6-116">Remarks</span></span>

<span data-ttu-id="a68d6-117">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Liste von Speicherorten vorhanden sind, `Int[]` die das Unterelement definieren.</span><span class="sxs-lookup"><span data-stu-id="a68d6-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a list of locations `Int[]` defining the subarray.</span></span>
<span data-ttu-id="a68d6-118">Die Erstellung des Unterarrays ist eine, die auf der Erstellung einer neuen Deep-Kopie des angegebenen Arrays basiert, anstatt Verweise beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="a68d6-118">The construction of the subarray is a based on generating a new, deep copy of the given array as opposed to maintaining references.</span></span>

<span data-ttu-id="a68d6-119">Wenn `Length(indices) < Length(array)` , wird von dieser Funktion eine Teilmenge von zurückgegeben `array` .</span><span class="sxs-lookup"><span data-stu-id="a68d6-119">If `Length(indices) < Length(array)`, this function will return a subset of `array`.</span></span> <span data-ttu-id="a68d6-120">Wenn dagegen `indices` wiederholte Elemente enthält, werden die entsprechenden Elemente von `array` ebenfalls wiederholt.</span><span class="sxs-lookup"><span data-stu-id="a68d6-120">On the other hand, if `indices` contains repeated elements, the corresponding elements of `array` will likewise be repeated.</span></span>
<span data-ttu-id="a68d6-121">Wenn `indices` und `array` dieselbe Länge aufweisen, stellt diese Funktion Permutationen von bereit `array` .</span><span class="sxs-lookup"><span data-stu-id="a68d6-121">If `indices` and `array` are the same length, this function provides permutations of `array`.</span></span>