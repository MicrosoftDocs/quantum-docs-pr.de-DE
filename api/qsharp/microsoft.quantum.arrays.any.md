---
uid: Microsoft.Quantum.Arrays.Any
title: Beliebige Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: dd5639f1b0a76cb356c89aca0c0e02d375f30d12
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706178"
---
# <a name="any-function"></a><span data-ttu-id="7ceca-102">Beliebige Funktion</span><span class="sxs-lookup"><span data-stu-id="7ceca-102">Any function</span></span>

<span data-ttu-id="7ceca-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7ceca-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7ceca-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7ceca-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7ceca-105">Bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, wird von überprüft, ob mindestens ein Element des Arrays dem Prädikat entspricht.</span><span class="sxs-lookup"><span data-stu-id="7ceca-105">Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.</span></span>

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="7ceca-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ceca-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="7ceca-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7ceca-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7ceca-108">Eine Funktion von `'T` zu `Bool` , die zum Überprüfen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ceca-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="7ceca-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="7ceca-109">array : 'T[]</span></span>

<span data-ttu-id="7ceca-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="7ceca-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="7ceca-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7ceca-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7ceca-112">Ein `Bool` Wert der-oder-Funktion des-Prädikats, das auf alle-Elemente angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ceca-112">A `Bool` value of the OR function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7ceca-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7ceca-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7ceca-114">GIF</span><span class="sxs-lookup"><span data-stu-id="7ceca-114">'T</span></span>

<span data-ttu-id="7ceca-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="7ceca-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ceca-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7ceca-116">Remarks</span></span>

<span data-ttu-id="7ceca-117">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `predicate: 'T -> Bool` können wir einen Wert entwickeln, `Bool` der angibt, ob ein Element übereinstimmt `predicate` .</span><span class="sxs-lookup"><span data-stu-id="7ceca-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if some element satisfies `predicate`.</span></span>