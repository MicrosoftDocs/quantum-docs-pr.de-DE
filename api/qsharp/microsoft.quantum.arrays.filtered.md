---
uid: Microsoft.Quantum.Arrays.Filtered
title: Gefilterte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 83336b7001ce1d8ab1f5340b194abdcf93588c31
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847162"
---
# <a name="filtered-function"></a><span data-ttu-id="ae2f2-102">Gefilterte Funktion</span><span class="sxs-lookup"><span data-stu-id="ae2f2-102">Filtered function</span></span>

<span data-ttu-id="ae2f2-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ae2f2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ae2f2-105">Bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, wird ein Array zurückgegeben, das aus den Elementen besteht, die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="ae2f2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ae2f2-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="ae2f2-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ae2f2-108">Eine Funktion von `'T` zu einem booleschen Wert, der zum Filtern von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="ae2f2-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="ae2f2-109">array : 'T[]</span></span>

<span data-ttu-id="ae2f2-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="ae2f2-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="ae2f2-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="ae2f2-111">Output : 'T[]</span></span>

<span data-ttu-id="ae2f2-112">Ein Array `'T[]` von-Elementen, die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ae2f2-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ae2f2-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ae2f2-114">GIF</span><span class="sxs-lookup"><span data-stu-id="ae2f2-114">'T</span></span>

<span data-ttu-id="ae2f2-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="ae2f2-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ae2f2-116">Example</span></span>

<span data-ttu-id="ae2f2-117">Der folgende Code veranschaulicht die "gefilterte" Funktion.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-117">The following code demonstrates the "Filtered" function.</span></span>
<span data-ttu-id="ae2f2-118">Ein Prädikat wird mithilfe der- @"microsoft.quantum.logical.greaterthani" Funktion definiert:</span><span class="sxs-lookup"><span data-stu-id="ae2f2-118">A predicate is defined using the @"microsoft.quantum.logical.greaterthani" function:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function FilteredDemo() : Unit {
   let predicate = GreaterThanI(_, 5);
   let filteredArray = Filtered(predicate, [2, 5, 9, 1, 8]);
   Message($"{filteredArray}");
}
```

<span data-ttu-id="ae2f2-119">Das Ergebnis, das in diesem Beispiel erwartet wird, ist ein Array von Zahlen größer als 5.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-119">The outcome one should expect from this example will be an array of numbers greater than 5.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2f2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae2f2-120">Remarks</span></span>

<span data-ttu-id="ae2f2-121">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und ein Prädikat vorhanden sind, `'T -> Bool` können Elemente gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-121">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>