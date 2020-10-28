---
uid: Microsoft.Quantum.Arrays.All
title: All-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 345c3fb92babd4ae2e54803b6c3b79b3313ef417
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706183"
---
# <a name="all-function"></a><span data-ttu-id="f2e57-102">All-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2e57-102">All function</span></span>

<span data-ttu-id="f2e57-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f2e57-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f2e57-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f2e57-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f2e57-105">Bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, und überprüft, ob alle Elemente des Arrays dem Prädikat entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f2e57-105">Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.</span></span>

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="f2e57-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2e57-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="f2e57-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f2e57-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f2e57-108">Eine Funktion von `'T` zu `Bool` , die zum Überprüfen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2e57-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="f2e57-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="f2e57-109">array : 'T[]</span></span>

<span data-ttu-id="f2e57-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="f2e57-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f2e57-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f2e57-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f2e57-112">Ein `Bool` Wert der and-Funktion des Prädikats, das auf alle-Elemente angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2e57-112">A `Bool` value of the AND function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f2e57-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f2e57-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f2e57-114">GIF</span><span class="sxs-lookup"><span data-stu-id="f2e57-114">'T</span></span>

<span data-ttu-id="f2e57-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="f2e57-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2e57-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2e57-116">Remarks</span></span>

<span data-ttu-id="f2e57-117">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `predicate: 'T -> Bool` können wir einen Wert entwickeln, `Bool` der angibt, ob alle Elemente erfüllen `predicate` .</span><span class="sxs-lookup"><span data-stu-id="f2e57-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if all elements satisfy `predicate`.</span></span>