---
uid: Microsoft.Quantum.Arrays.All
title: All-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: a7c83e38c3c101b712215eb664486fe29863a52b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221690"
---
# <a name="all-function"></a><span data-ttu-id="32860-102">All-Funktion</span><span class="sxs-lookup"><span data-stu-id="32860-102">All function</span></span>

<span data-ttu-id="32860-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="32860-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="32860-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="32860-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="32860-105">Bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, und überprüft, ob alle Elemente des Arrays dem Prädikat entsprechen.</span><span class="sxs-lookup"><span data-stu-id="32860-105">Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.</span></span>

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="32860-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="32860-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="32860-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="32860-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="32860-108">Eine Funktion von `'T` zu `Bool` , die zum Überprüfen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="32860-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="32860-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="32860-109">array : 'T[]</span></span>

<span data-ttu-id="32860-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="32860-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="32860-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="32860-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="32860-112">Ein `Bool` Wert der and-Funktion des Prädikats, das auf alle-Elemente angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="32860-112">A `Bool` value of the AND function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="32860-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="32860-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="32860-114">GIF</span><span class="sxs-lookup"><span data-stu-id="32860-114">'T</span></span>

<span data-ttu-id="32860-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="32860-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="32860-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32860-116">Remarks</span></span>

<span data-ttu-id="32860-117">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `predicate: 'T -> Bool` können wir einen Wert entwickeln, `Bool` der angibt, ob alle Elemente erfüllen `predicate` .</span><span class="sxs-lookup"><span data-stu-id="32860-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if all elements satisfy `predicate`.</span></span>