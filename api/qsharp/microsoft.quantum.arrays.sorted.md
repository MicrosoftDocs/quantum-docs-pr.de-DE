---
uid: Microsoft.Quantum.Arrays.Sorted
title: Sortierte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: 14ac5325b81aec4ba0bf94a83cf00e086a075a7c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705786"
---
# <a name="sorted-function"></a><span data-ttu-id="f7f1b-102">Sortierte Funktion</span><span class="sxs-lookup"><span data-stu-id="f7f1b-102">Sorted function</span></span>

<span data-ttu-id="f7f1b-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f7f1b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f7f1b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f7f1b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f7f1b-105">Gibt bei Angabe eines Arrays die Elemente dieses Arrays nach einer angegebenen Vergleichsfunktion sortiert zurück.</span><span class="sxs-lookup"><span data-stu-id="f7f1b-105">Given an array, returns the elements of that array sorted by a given comparison function.</span></span>

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="f7f1b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7f1b-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="f7f1b-107">Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f7f1b-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f7f1b-108">Eine Funktion, die zwei-Elemente als vergleicht, die `a` als kleiner oder gleich angesehen werden, `b` wenn gleich `comparison(a, b)` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="f7f1b-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="f7f1b-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="f7f1b-109">array : 'T[]</span></span>

<span data-ttu-id="f7f1b-110">Das Array, das sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7f1b-110">The array to be sorted.</span></span>



## <a name="output--t"></a><span data-ttu-id="f7f1b-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="f7f1b-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f7f1b-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f7f1b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f7f1b-113">GIF</span><span class="sxs-lookup"><span data-stu-id="f7f1b-113">'T</span></span>

<span data-ttu-id="f7f1b-114">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="f7f1b-114">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7f1b-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7f1b-115">Remarks</span></span>

<span data-ttu-id="f7f1b-116">Es wird `comparison` davon ausgegangen, dass die Funktion transitiv ist, sodass, wenn `comparison(a, b)` und `comparison(b, c)` , `comparison(a, c)` angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="f7f1b-116">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="f7f1b-117">Wenn diese Eigenschaft nicht enthalten ist, ist die Ausgabe dieser Funktion möglicherweise falsch.</span><span class="sxs-lookup"><span data-stu-id="f7f1b-117">If this property does not hold, then the output of this function may be incorrect.</span></span>

<span data-ttu-id="f7f1b-118">Da es sich um eine Funktion handelt, sind die Ergebnisse vollständig deternistisch, auch wenn zwei Elemente als gleich betrachtet werden, d `comparison` . h., wenn `comparison(a, b)` und `comparison(b, a)` beide sind `true` .</span><span class="sxs-lookup"><span data-stu-id="f7f1b-118">As this is a function, the results are completely determinstic, even when two elements are considered equal under `comparison`; that is, when `comparison(a, b)` and `comparison(b, a)` are both `true`.</span></span>
<span data-ttu-id="f7f1b-119">Insbesondere wird sichergestellt, dass die von dieser Funktion ausgeführte Sortierung stabil ist, sodass, wenn zwei `a` Elemente `b` in dieser Reihenfolge innerhalb von auftreten `array` und als gleich betrachtet werden `comparison` , `a` auch vor `b` in der Ausgabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f7f1b-119">In particular, the sort performed by this function is guaranteed to be stable, so that if two elements `a` and `b` occur in that order within `array` and are considered equal under `comparison`, then `a` will also appear before `b` in the output.</span></span>

<span data-ttu-id="f7f1b-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f7f1b-120">For example:</span></span>

```Q#
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```