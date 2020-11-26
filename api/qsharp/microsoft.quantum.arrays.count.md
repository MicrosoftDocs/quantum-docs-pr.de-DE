---
uid: Microsoft.Quantum.Arrays.Count
title: Count-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 48b75cc6d6584f899223a0803f31fd174836f303
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221554"
---
# <a name="count-function"></a><span data-ttu-id="ef688-102">Count-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef688-102">Count function</span></span>

<span data-ttu-id="ef688-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ef688-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ef688-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef688-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef688-105">Gibt bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, die Anzahl der Elemente eines Arrays zurück, das aus den Elementen besteht, die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ef688-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="ef688-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ef688-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="ef688-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ef688-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ef688-108">Eine Funktion von `'T` zu einem booleschen Wert, der zum Filtern von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef688-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="ef688-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="ef688-109">array : 'T[]</span></span>

<span data-ttu-id="ef688-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="ef688-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="ef688-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ef688-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ef688-112">Die Anzahl der Elemente in `array` , die das Prädikat erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ef688-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ef688-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ef688-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ef688-114">GIF</span><span class="sxs-lookup"><span data-stu-id="ef688-114">'T</span></span>

<span data-ttu-id="ef688-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="ef688-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef688-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef688-116">Remarks</span></span>

<span data-ttu-id="ef688-117">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und ein Prädikat vorhanden sind, `'T -> Bool` können Elemente gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="ef688-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>