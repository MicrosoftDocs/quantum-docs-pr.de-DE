---
uid: Microsoft.Quantum.Arrays.Subarray
title: Subarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: be7b6ee1a396d67ebc311d8d97f4bd751a32d171
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705759"
---
# <a name="subarray-function"></a><span data-ttu-id="d9413-102">Subarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9413-102">Subarray function</span></span>

<span data-ttu-id="d9413-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d9413-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d9413-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d9413-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d9413-105">Nimmt ein Array und eine Liste von Speicherorten an und erstellt ein neues Array, das aus den Elementen des ursprünglichen Arrays gebildet wird, die den angegebenen Speicherorten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d9413-105">Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.</span></span>

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="d9413-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9413-106">Input</span></span>

### <a name="indices--int"></a><span data-ttu-id="d9413-107">Indizes: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d9413-107">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d9413-108">Eine Liste von ganzen Zahlen, die zum Definieren des Unterarrays verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9413-108">A list of integers that is used to define the subarray.</span></span>


### <a name="array--t"></a><span data-ttu-id="d9413-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="d9413-109">array : 'T[]</span></span>

<span data-ttu-id="d9413-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="d9413-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="d9413-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="d9413-111">Output : 'T[]</span></span>

<span data-ttu-id="d9413-112">Ein Array `out` von-Elementen, deren Indizes dem Unterarray entsprechen, z `out[idx] == array[indices[idx]]` . b..</span><span class="sxs-lookup"><span data-stu-id="d9413-112">An array `out` of elements whose indices correspond to the subarray, such that `out[idx] == array[indices[idx]]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d9413-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d9413-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d9413-114">GIF</span><span class="sxs-lookup"><span data-stu-id="d9413-114">'T</span></span>

<span data-ttu-id="d9413-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="d9413-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9413-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9413-116">Remarks</span></span>

<span data-ttu-id="d9413-117">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Liste von Speicherorten vorhanden sind, `Int[]` die das Unterelement definieren.</span><span class="sxs-lookup"><span data-stu-id="d9413-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a list of locations `Int[]` defining the subarray.</span></span>
<span data-ttu-id="d9413-118">Die Erstellung des Unterarrays ist eine, die auf der Erstellung einer neuen Deep-Kopie des angegebenen Arrays basiert, anstatt Verweise beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="d9413-118">The construction of the subarray is a based on generating a new, deep copy of the given array as opposed to maintaining references.</span></span>

<span data-ttu-id="d9413-119">Wenn `Length(indices) < Length(array)` , wird von dieser Funktion eine Teilmenge von zurückgegeben `array` .</span><span class="sxs-lookup"><span data-stu-id="d9413-119">If `Length(indices) < Length(array)`, this function will return a subset of `array`.</span></span> <span data-ttu-id="d9413-120">Wenn dagegen `indices` wiederholte Elemente enthält, werden die entsprechenden Elemente von `array` ebenfalls wiederholt.</span><span class="sxs-lookup"><span data-stu-id="d9413-120">On the other hand, if `indices` contains repeated elements, the corresponding elements of `array` will likewise be repeated.</span></span>
<span data-ttu-id="d9413-121">Wenn `indices` und `array` dieselbe Länge aufweisen, stellt diese Funktion Permutationen von bereit `array` .</span><span class="sxs-lookup"><span data-stu-id="d9413-121">If `indices` and `array` are the same length, this function provides permutations of `array`.</span></span>