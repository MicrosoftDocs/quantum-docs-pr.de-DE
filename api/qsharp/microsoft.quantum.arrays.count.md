---
uid: Microsoft.Quantum.Arrays.Count
title: Count-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 408a4a42dda6a4827db6d5865e2b4b8a8df5b37a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706130"
---
# <a name="count-function"></a><span data-ttu-id="dbac1-102">Count-Funktion</span><span class="sxs-lookup"><span data-stu-id="dbac1-102">Count function</span></span>

<span data-ttu-id="dbac1-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dbac1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dbac1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dbac1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dbac1-105">Gibt bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, die Anzahl der Elemente eines Arrays zurück, das aus den Elementen besteht, die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="dbac1-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="dbac1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dbac1-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="dbac1-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="dbac1-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="dbac1-108">Eine Funktion von `'T` zu einem booleschen Wert, der zum Filtern von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbac1-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="dbac1-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="dbac1-109">array : 'T[]</span></span>

<span data-ttu-id="dbac1-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="dbac1-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="dbac1-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dbac1-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dbac1-112">Die Anzahl der Elemente in `array` , die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="dbac1-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dbac1-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="dbac1-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dbac1-114">GIF</span><span class="sxs-lookup"><span data-stu-id="dbac1-114">'T</span></span>

<span data-ttu-id="dbac1-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="dbac1-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbac1-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dbac1-116">Remarks</span></span>

<span data-ttu-id="dbac1-117">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und ein Prädikat vorhanden sind, `'T -> Bool` können Elemente gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="dbac1-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>