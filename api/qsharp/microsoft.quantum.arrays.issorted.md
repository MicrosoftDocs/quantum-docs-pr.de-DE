---
uid: Microsoft.Quantum.Arrays.IsSorted
title: IsSorted-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: 330c1f789585f64cf255bc74f8a9c1ccf81b009e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705930"
---
# <a name="issorted-function"></a><span data-ttu-id="39999-102">IsSorted-Funktion</span><span class="sxs-lookup"><span data-stu-id="39999-102">IsSorted function</span></span>

<span data-ttu-id="39999-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="39999-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="39999-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="39999-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="39999-105">Gibt bei Angabe eines Arrays zurück, ob dieses Array entsprechend der Definition durch eine angegebene Vergleichsfunktion sortiert wird.</span><span class="sxs-lookup"><span data-stu-id="39999-105">Given an array, returns whether that array is sorted as defined by a given comparison function.</span></span>

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="39999-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39999-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="39999-107">Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="39999-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="39999-108">Eine Funktion, die zwei-Elemente als vergleicht, die `a` als kleiner oder gleich angesehen werden, `b` wenn gleich `comparison(a, b)` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="39999-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="39999-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="39999-109">array : 'T[]</span></span>

<span data-ttu-id="39999-110">Das zu überprüfende Array.</span><span class="sxs-lookup"><span data-stu-id="39999-110">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="39999-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="39999-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="39999-112">`true` Wenn für jedes Element Paar `a` und `b` `array` das Vorkommen in dieser Reihenfolge `comparison(a, b)` ist, ist `true` .</span><span class="sxs-lookup"><span data-stu-id="39999-112">`true` if and only if for each pair of elements `a` and `b` of `array` occuring in that order, `comparison(a, b)` is `true`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="39999-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="39999-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="39999-114">GIF</span><span class="sxs-lookup"><span data-stu-id="39999-114">'T</span></span>

<span data-ttu-id="39999-115">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="39999-115">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="39999-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39999-116">Remarks</span></span>

<span data-ttu-id="39999-117">Es wird `comparison` davon ausgegangen, dass die Funktion transitiv ist, sodass, wenn `comparison(a, b)` und `comparison(b, c)` , `comparison(a, c)` angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="39999-117">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="39999-118">Wenn diese Eigenschaft nicht enthalten ist, ist die Ausgabe dieser Funktion möglicherweise falsch.</span><span class="sxs-lookup"><span data-stu-id="39999-118">If this property does not hold, then the output of this function may be incorrect.</span></span>