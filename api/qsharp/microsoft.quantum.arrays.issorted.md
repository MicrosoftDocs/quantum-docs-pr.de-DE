---
uid: Microsoft.Quantum.Arrays.IsSorted
title: IsSorted-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: b2c5f11c0d92ddf9214de2d439c175319c569be0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220831"
---
# <a name="issorted-function"></a><span data-ttu-id="ba8ed-102">IsSorted-Funktion</span><span class="sxs-lookup"><span data-stu-id="ba8ed-102">IsSorted function</span></span>

<span data-ttu-id="ba8ed-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ba8ed-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ba8ed-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ba8ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ba8ed-105">Gibt bei Angabe eines Arrays zurück, ob dieses Array entsprechend der Definition durch eine angegebene Vergleichsfunktion sortiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba8ed-105">Given an array, returns whether that array is sorted as defined by a given comparison function.</span></span>

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="ba8ed-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba8ed-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="ba8ed-107">Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ba8ed-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ba8ed-108">Eine Funktion, die zwei-Elemente als vergleicht, die `a` als kleiner oder gleich angesehen werden, `b` wenn gleich `comparison(a, b)` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="ba8ed-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="ba8ed-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="ba8ed-109">array : 'T[]</span></span>

<span data-ttu-id="ba8ed-110">Das zu überprüfende Array.</span><span class="sxs-lookup"><span data-stu-id="ba8ed-110">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ba8ed-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ba8ed-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ba8ed-112">`true` Wenn für jedes Element Paar `a` und `b` `array` das Vorkommen in dieser Reihenfolge `comparison(a, b)` ist, ist `true` .</span><span class="sxs-lookup"><span data-stu-id="ba8ed-112">`true` if and only if for each pair of elements `a` and `b` of `array` occuring in that order, `comparison(a, b)` is `true`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ba8ed-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ba8ed-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ba8ed-114">GIF</span><span class="sxs-lookup"><span data-stu-id="ba8ed-114">'T</span></span>

<span data-ttu-id="ba8ed-115">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="ba8ed-115">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba8ed-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba8ed-116">Remarks</span></span>

<span data-ttu-id="ba8ed-117">Es wird `comparison` davon ausgegangen, dass die Funktion transitiv ist, sodass, wenn `comparison(a, b)` und `comparison(b, c)` , `comparison(a, c)` angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="ba8ed-117">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="ba8ed-118">Wenn diese Eigenschaft nicht enthalten ist, ist die Ausgabe dieser Funktion möglicherweise falsch.</span><span class="sxs-lookup"><span data-stu-id="ba8ed-118">If this property does not hold, then the output of this function may be incorrect.</span></span>