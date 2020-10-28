---
uid: Microsoft.Quantum.Arrays.Filtered
title: Gefilterte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 4c786c69b0896b517f108611e32501867838aeb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706042"
---
# <a name="filtered-function"></a><span data-ttu-id="20e65-102">Gefilterte Funktion</span><span class="sxs-lookup"><span data-stu-id="20e65-102">Filtered function</span></span>

<span data-ttu-id="20e65-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="20e65-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="20e65-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="20e65-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="20e65-105">Bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, wird ein Array zurückgegeben, das aus den Elementen besteht, die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="20e65-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="20e65-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20e65-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="20e65-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="20e65-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="20e65-108">Eine Funktion von `'T` zu einem booleschen Wert, der zum Filtern von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20e65-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="20e65-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="20e65-109">array : 'T[]</span></span>

<span data-ttu-id="20e65-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="20e65-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="20e65-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="20e65-111">Output : 'T[]</span></span>

<span data-ttu-id="20e65-112">Ein Array `'T[]` von-Elementen, die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="20e65-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="20e65-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="20e65-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="20e65-114">GIF</span><span class="sxs-lookup"><span data-stu-id="20e65-114">'T</span></span>

<span data-ttu-id="20e65-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="20e65-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="20e65-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20e65-116">Remarks</span></span>

<span data-ttu-id="20e65-117">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und ein Prädikat vorhanden sind, `'T -> Bool` können Elemente gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="20e65-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>