---
uid: Microsoft.Quantum.Arrays.Unique
title: Unique-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: 7964d5d41eb68cb05f9414164d69496c1f76eb08
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220007"
---
# <a name="unique-function"></a><span data-ttu-id="53fd5-102">Unique-Funktion</span><span class="sxs-lookup"><span data-stu-id="53fd5-102">Unique function</span></span>

<span data-ttu-id="53fd5-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="53fd5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="53fd5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="53fd5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="53fd5-105">Gibt ein neues Array zurück, das keine gleich benachbarten Elemente aufweist.</span><span class="sxs-lookup"><span data-stu-id="53fd5-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="53fd5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53fd5-106">Description</span></span>

<span data-ttu-id="53fd5-107">Bei einem bestimmten Array von Elementen und einer Funktion zum Testen der Gleichheit gibt diese Funktion ein neues Array zurück, in dem die relative Reihenfolge der Elemente beibehalten wird. alle angrenzenden Elemente, die gleich sind, werden jedoch nur nach einem einzelnen Element gefiltert.</span><span class="sxs-lookup"><span data-stu-id="53fd5-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="53fd5-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53fd5-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="53fd5-109">gleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="53fd5-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="53fd5-110">Eine Funktion, die zwei-Elemente als vergleicht, die `a` als gleich betrachtet werden, `b` wenn gleich `equal(a, b)` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="53fd5-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="53fd5-111">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="53fd5-111">array : 'T[]</span></span>

<span data-ttu-id="53fd5-112">Das Array, das nach eindeutigen Elementen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="53fd5-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="53fd5-113">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="53fd5-113">Output : 'T[]</span></span>

<span data-ttu-id="53fd5-114">Array ohne gleich angrenzende Elemente.</span><span class="sxs-lookup"><span data-stu-id="53fd5-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="53fd5-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="53fd5-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="53fd5-116">GIF</span><span class="sxs-lookup"><span data-stu-id="53fd5-116">'T</span></span>

<span data-ttu-id="53fd5-117">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="53fd5-117">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="53fd5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53fd5-118">Remarks</span></span>

<span data-ttu-id="53fd5-119">Wenn mehrere Elemente gleich sind, jedoch nicht nebeneinander, werden mehrere Vorkommen im Ausgabe Array angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53fd5-119">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="53fd5-120">Verwenden Sie diese Funktion in Verbindung mit `Sorted` , um ein Array mit Gesamtzahl der eindeutigen Elemente zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="53fd5-120">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>