---
uid: Microsoft.Quantum.Arrays.Unique
title: Unique-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: c5d40bb82f2de640e9c78eef0c27e4766b477826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705719"
---
# <a name="unique-function"></a><span data-ttu-id="518eb-102">Unique-Funktion</span><span class="sxs-lookup"><span data-stu-id="518eb-102">Unique function</span></span>

<span data-ttu-id="518eb-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="518eb-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="518eb-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="518eb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="518eb-105">Gibt ein neues Array zurück, das keine gleich benachbarten Elemente aufweist.</span><span class="sxs-lookup"><span data-stu-id="518eb-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="518eb-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="518eb-106">Description</span></span>

<span data-ttu-id="518eb-107">Bei einem bestimmten Array von Elementen und einer Funktion zum Testen der Gleichheit gibt diese Funktion ein neues Array zurück, in dem die relative Reihenfolge der Elemente beibehalten wird. alle angrenzenden Elemente, die gleich sind, werden jedoch nur nach einem einzelnen Element gefiltert.</span><span class="sxs-lookup"><span data-stu-id="518eb-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="518eb-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="518eb-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="518eb-109">gleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="518eb-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="518eb-110">Eine Funktion, die zwei-Elemente als vergleicht, die `a` als gleich betrachtet werden, `b` wenn gleich `equal(a, b)` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="518eb-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="518eb-111">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="518eb-111">array : 'T[]</span></span>

<span data-ttu-id="518eb-112">Das Array, das nach eindeutigen Elementen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="518eb-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="518eb-113">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="518eb-113">Output : 'T[]</span></span>

<span data-ttu-id="518eb-114">Array ohne gleich angrenzende Elemente.</span><span class="sxs-lookup"><span data-stu-id="518eb-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="518eb-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="518eb-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="518eb-116">GIF</span><span class="sxs-lookup"><span data-stu-id="518eb-116">'T</span></span>

<span data-ttu-id="518eb-117">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="518eb-117">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="518eb-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="518eb-118">Remarks</span></span>

<span data-ttu-id="518eb-119">Wenn mehrere Elemente gleich sind, jedoch nicht nebeneinander, werden mehrere Vorkommen im Ausgabe Array angezeigt.</span><span class="sxs-lookup"><span data-stu-id="518eb-119">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="518eb-120">Verwenden Sie diese Funktion in Verbindung mit `Sorted` , um ein Array mit Gesamtzahl der eindeutigen Elemente zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="518eb-120">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>