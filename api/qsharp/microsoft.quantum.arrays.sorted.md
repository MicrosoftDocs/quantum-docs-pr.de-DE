---
uid: Microsoft.Quantum.Arrays.Sorted
title: Sortierte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: cb8a1ef438d798c8201ed9f52677e253770df1d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845447"
---
# <a name="sorted-function"></a><span data-ttu-id="866c4-102">Sortierte Funktion</span><span class="sxs-lookup"><span data-stu-id="866c4-102">Sorted function</span></span>

<span data-ttu-id="866c4-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="866c4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="866c4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="866c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="866c4-105">Gibt bei Angabe eines Arrays die Elemente dieses Arrays nach einer angegebenen Vergleichsfunktion sortiert zurück.</span><span class="sxs-lookup"><span data-stu-id="866c4-105">Given an array, returns the elements of that array sorted by a given comparison function.</span></span>

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="866c4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="866c4-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="866c4-107">Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="866c4-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="866c4-108">Eine Funktion, die zwei-Elemente als vergleicht, die `a` als kleiner oder gleich angesehen werden, `b` wenn gleich `comparison(a, b)` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="866c4-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="866c4-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="866c4-109">array : 'T[]</span></span>

<span data-ttu-id="866c4-110">Das Array, das sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="866c4-110">The array to be sorted.</span></span>



## <a name="output--t"></a><span data-ttu-id="866c4-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="866c4-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="866c4-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="866c4-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="866c4-113">GIF</span><span class="sxs-lookup"><span data-stu-id="866c4-113">'T</span></span>

<span data-ttu-id="866c4-114">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="866c4-114">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="866c4-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="866c4-115">Example</span></span>

<span data-ttu-id="866c4-116">Im folgenden Code Ausschnitt wird ein Array aus ganzen Zahlen sortiert, das in aufsteigender Reihenfolge auftreten soll:</span><span class="sxs-lookup"><span data-stu-id="866c4-116">The following snippet sorts an array of integers to occur in ascending order:</span></span>

```qsharp
let sortedArray = Sorted(LessThanOrEqualI, [3, 17, 11, -201, -11]);
```

## <a name="remarks"></a><span data-ttu-id="866c4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="866c4-117">Remarks</span></span>

<span data-ttu-id="866c4-118">Es wird `comparison` davon ausgegangen, dass die Funktion transitiv ist, sodass, wenn `comparison(a, b)` und `comparison(b, c)` , `comparison(a, c)` angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="866c4-118">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="866c4-119">Wenn diese Eigenschaft nicht enthalten ist, ist die Ausgabe dieser Funktion möglicherweise falsch.</span><span class="sxs-lookup"><span data-stu-id="866c4-119">If this property does not hold, then the output of this function may be incorrect.</span></span>

<span data-ttu-id="866c4-120">Da es sich um eine Funktion handelt, sind die Ergebnisse vollständig deternistisch, auch wenn zwei Elemente als gleich betrachtet werden, d `comparison` . h., wenn `comparison(a, b)` und `comparison(b, a)` beide sind `true` .</span><span class="sxs-lookup"><span data-stu-id="866c4-120">As this is a function, the results are completely determinstic, even when two elements are considered equal under `comparison`; that is, when `comparison(a, b)` and `comparison(b, a)` are both `true`.</span></span>
<span data-ttu-id="866c4-121">Insbesondere wird sichergestellt, dass die von dieser Funktion ausgeführte Sortierung stabil ist, sodass, wenn zwei `a` Elemente `b` in dieser Reihenfolge innerhalb von auftreten `array` und als gleich betrachtet werden `comparison` , `a` auch vor `b` in der Ausgabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="866c4-121">In particular, the sort performed by this function is guaranteed to be stable, so that if two elements `a` and `b` occur in that order within `array` and are considered equal under `comparison`, then `a` will also appear before `b` in the output.</span></span>

<span data-ttu-id="866c4-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="866c4-122">For example:</span></span>

```qsharp
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