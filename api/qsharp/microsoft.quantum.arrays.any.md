---
uid: Microsoft.Quantum.Arrays.Any
title: Beliebige Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: a05f9531168bf2b32977665d38cc00f3c8e64879
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846281"
---
# <a name="any-function"></a><span data-ttu-id="598fe-102">Beliebige Funktion</span><span class="sxs-lookup"><span data-stu-id="598fe-102">Any function</span></span>

<span data-ttu-id="598fe-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="598fe-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="598fe-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="598fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="598fe-105">Bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, wird von überprüft, ob mindestens ein Element des Arrays dem Prädikat entspricht.</span><span class="sxs-lookup"><span data-stu-id="598fe-105">Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.</span></span>

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="598fe-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="598fe-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="598fe-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="598fe-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="598fe-108">Eine Funktion von `'T` zu `Bool` , die zum Überprüfen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="598fe-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="598fe-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="598fe-109">array : 'T[]</span></span>

<span data-ttu-id="598fe-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="598fe-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="598fe-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="598fe-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="598fe-112">Ein `Bool` Wert der-oder-Funktion des-Prädikats, das auf alle-Elemente angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="598fe-112">A `Bool` value of the OR function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="598fe-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="598fe-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="598fe-114">GIF</span><span class="sxs-lookup"><span data-stu-id="598fe-114">'T</span></span>

<span data-ttu-id="598fe-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="598fe-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="598fe-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="598fe-116">Example</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function IsThreePresent() : Bool {
    let arrayOfInts = [1, 2, 3, 4, 5];
    let is3Present = IsNumberPresentInArray(3, arrayOfInts);
    return is3Present;
}

function IsNumberPresentInArray(n : Int, array : Int[]) : Bool {
    return Any(EqualI(_, n), array);
}
```

## <a name="remarks"></a><span data-ttu-id="598fe-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="598fe-117">Remarks</span></span>

<span data-ttu-id="598fe-118">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `predicate: 'T -> Bool` können wir einen Wert entwickeln, `Bool` der angibt, ob ein Element übereinstimmt `predicate` .</span><span class="sxs-lookup"><span data-stu-id="598fe-118">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if some element satisfies `predicate`.</span></span>