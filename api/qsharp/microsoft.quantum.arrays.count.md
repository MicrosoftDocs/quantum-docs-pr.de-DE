---
uid: Microsoft.Quantum.Arrays.Count
title: Count-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: e178ee63526e3485e8cc83a3ba8f827d8ecac552
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842848"
---
# <a name="count-function"></a><span data-ttu-id="af997-102">Count-Funktion</span><span class="sxs-lookup"><span data-stu-id="af997-102">Count function</span></span>

<span data-ttu-id="af997-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="af997-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="af997-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="af997-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="af997-105">Gibt bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, die Anzahl der Elemente eines Arrays zurück, das aus den Elementen besteht, die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="af997-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="af997-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="af997-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="af997-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="af997-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="af997-108">Eine Funktion von `'T` zu einem booleschen Wert, der zum Filtern von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af997-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="af997-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="af997-109">array : 'T[]</span></span>

<span data-ttu-id="af997-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="af997-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="af997-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="af997-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="af997-112">Die Anzahl der Elemente in `array` , die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="af997-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="af997-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="af997-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="af997-114">GIF</span><span class="sxs-lookup"><span data-stu-id="af997-114">'T</span></span>

<span data-ttu-id="af997-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="af997-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="af997-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="af997-116">Example</span></span>

<span data-ttu-id="af997-117">Der folgende Code veranschaulicht die "count"-Funktion.</span><span class="sxs-lookup"><span data-stu-id="af997-117">The following code demonstrates the "Count" function.</span></span>
<span data-ttu-id="af997-118">Ein Prädikat wird mithilfe der- @"microsoft.quantum.logical.greaterthani" Funktion definiert:</span><span class="sxs-lookup"><span data-stu-id="af997-118">A predicate is defined using the @"microsoft.quantum.logical.greaterthani" function:</span></span>

```qsharp
 let predicate = GreaterThanI(_, 5);
 let count = Count(predicate, [2, 5, 9, 1, 8]);
 // count = 2
```

## <a name="remarks"></a><span data-ttu-id="af997-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af997-119">Remarks</span></span>

<span data-ttu-id="af997-120">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und ein Prädikat vorhanden sind, `'T -> Bool` können Elemente gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="af997-120">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>