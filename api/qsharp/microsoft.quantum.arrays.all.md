---
uid: Microsoft.Quantum.Arrays.All
title: All-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 17e61ea161b90fe089b7df7c10188d604d72dcfa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842896"
---
# <a name="all-function"></a><span data-ttu-id="635b5-102">All-Funktion</span><span class="sxs-lookup"><span data-stu-id="635b5-102">All function</span></span>

<span data-ttu-id="635b5-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="635b5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="635b5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="635b5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="635b5-105">Bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, und überprüft, ob alle Elemente des Arrays dem Prädikat entsprechen.</span><span class="sxs-lookup"><span data-stu-id="635b5-105">Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.</span></span>

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="635b5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="635b5-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="635b5-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="635b5-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="635b5-108">Eine Funktion von `'T` zu `Bool` , die zum Überprüfen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="635b5-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="635b5-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="635b5-109">array : 'T[]</span></span>

<span data-ttu-id="635b5-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="635b5-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="635b5-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="635b5-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="635b5-112">Ein `Bool` Wert der and-Funktion des Prädikats, das auf alle-Elemente angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="635b5-112">A `Bool` value of the AND function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="635b5-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="635b5-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="635b5-114">GIF</span><span class="sxs-lookup"><span data-stu-id="635b5-114">'T</span></span>

<span data-ttu-id="635b5-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="635b5-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="635b5-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="635b5-116">Example</span></span>

<span data-ttu-id="635b5-117">Der folgende Code überprüft, ob alle Elemente des Arrays ungleich 0 (null) sind:</span><span class="sxs-lookup"><span data-stu-id="635b5-117">The following code checks whether all elements of the array are non-zero:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function AllDemo() : Unit {
    let predicate = NotEqualI(_, 0);
    let isNonZero = All(predicate, [2, 3, 4, 5, 6, 0]);
    Message($"{isNonZero}");
}
```

## <a name="remarks"></a><span data-ttu-id="635b5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="635b5-118">Remarks</span></span>

<span data-ttu-id="635b5-119">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `predicate: 'T -> Bool` können wir einen Wert entwickeln, `Bool` der angibt, ob alle Elemente erfüllen `predicate` .</span><span class="sxs-lookup"><span data-stu-id="635b5-119">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if all elements satisfy `predicate`.</span></span>