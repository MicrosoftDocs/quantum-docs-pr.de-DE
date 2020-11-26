---
uid: Microsoft.Quantum.Arrays.Any
title: Beliebige Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: 717ab9ebcbb864a6faf1c14cd36125e589849f2e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221656"
---
# <a name="any-function"></a><span data-ttu-id="9a917-102">Beliebige Funktion</span><span class="sxs-lookup"><span data-stu-id="9a917-102">Any function</span></span>

<span data-ttu-id="9a917-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9a917-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9a917-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9a917-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9a917-105">Bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, wird von überprüft, ob mindestens ein Element des Arrays dem Prädikat entspricht.</span><span class="sxs-lookup"><span data-stu-id="9a917-105">Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.</span></span>

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="9a917-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a917-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="9a917-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9a917-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9a917-108">Eine Funktion von `'T` zu `Bool` , die zum Überprüfen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a917-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="9a917-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="9a917-109">array : 'T[]</span></span>

<span data-ttu-id="9a917-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="9a917-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9a917-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9a917-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9a917-112">Ein `Bool` Wert der-oder-Funktion des-Prädikats, das auf alle-Elemente angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a917-112">A `Bool` value of the OR function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9a917-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9a917-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9a917-114">GIF</span><span class="sxs-lookup"><span data-stu-id="9a917-114">'T</span></span>

<span data-ttu-id="9a917-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="9a917-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a917-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a917-116">Remarks</span></span>

<span data-ttu-id="9a917-117">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `predicate: 'T -> Bool` können wir einen Wert entwickeln, `Bool` der angibt, ob ein Element übereinstimmt `predicate` .</span><span class="sxs-lookup"><span data-stu-id="9a917-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if some element satisfies `predicate`.</span></span>