---
uid: Microsoft.Quantum.Arrays.IsSorted
title: IsSorted-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: a5916b5cbf36e1b6c421a81e04016a333e2b5be7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845737"
---
# <a name="issorted-function"></a><span data-ttu-id="490be-102">IsSorted-Funktion</span><span class="sxs-lookup"><span data-stu-id="490be-102">IsSorted function</span></span>

<span data-ttu-id="490be-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="490be-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="490be-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="490be-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="490be-105">Gibt bei Angabe eines Arrays zurück, ob dieses Array entsprechend der Definition durch eine angegebene Vergleichsfunktion sortiert wird.</span><span class="sxs-lookup"><span data-stu-id="490be-105">Given an array, returns whether that array is sorted as defined by a given comparison function.</span></span>

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="490be-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="490be-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="490be-107">Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="490be-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="490be-108">Eine Funktion, die zwei-Elemente als vergleicht, die `a` als kleiner oder gleich angesehen werden, `b` wenn gleich `comparison(a, b)` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="490be-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="490be-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="490be-109">array : 'T[]</span></span>

<span data-ttu-id="490be-110">Das zu überprüfende Array.</span><span class="sxs-lookup"><span data-stu-id="490be-110">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="490be-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="490be-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="490be-112">`true` Wenn für jedes Element Paar `a` und `b` `array` das Vorkommen in dieser Reihenfolge `comparison(a, b)` ist, ist `true` .</span><span class="sxs-lookup"><span data-stu-id="490be-112">`true` if and only if for each pair of elements `a` and `b` of `array` occuring in that order, `comparison(a, b)` is `true`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="490be-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="490be-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="490be-114">GIF</span><span class="sxs-lookup"><span data-stu-id="490be-114">'T</span></span>

<span data-ttu-id="490be-115">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="490be-115">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="490be-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="490be-116">Remarks</span></span>

<span data-ttu-id="490be-117">Es wird `comparison` davon ausgegangen, dass die Funktion transitiv ist, sodass, wenn `comparison(a, b)` und `comparison(b, c)` , `comparison(a, c)` angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="490be-117">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="490be-118">Wenn diese Eigenschaft nicht enthalten ist, ist die Ausgabe dieser Funktion möglicherweise falsch.</span><span class="sxs-lookup"><span data-stu-id="490be-118">If this property does not hold, then the output of this function may be incorrect.</span></span>