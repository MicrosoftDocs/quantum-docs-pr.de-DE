---
uid: Microsoft.Quantum.Arrays.Where
title: Where-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 97598aa25d2d085aaab94f3d60ee64db9e2b89d6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219922"
---
# <a name="where-function"></a><span data-ttu-id="02b67-102">Where-Funktion</span><span class="sxs-lookup"><span data-stu-id="02b67-102">Where function</span></span>

<span data-ttu-id="02b67-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="02b67-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="02b67-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="02b67-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="02b67-105">Gibt bei Angabe eines Prädikats und eines Arrays die Indizes dieses Arrays zurück, bei denen das Prädikat "true" ist.</span><span class="sxs-lookup"><span data-stu-id="02b67-105">Given a predicate and an array, returns the indices of that array where the predicate is true.</span></span>

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="02b67-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02b67-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="02b67-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="02b67-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="02b67-108">Eine Funktion von `'T` zu einem booleschen Wert, der zum Filtern von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02b67-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="02b67-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="02b67-109">array : 'T[]</span></span>

<span data-ttu-id="02b67-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="02b67-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="02b67-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="02b67-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="02b67-112">Ein Array von Indizes, bei denen " `predicate` true" ist.</span><span class="sxs-lookup"><span data-stu-id="02b67-112">An array of indices where `predicate` is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="02b67-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="02b67-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="02b67-114">GIF</span><span class="sxs-lookup"><span data-stu-id="02b67-114">'T</span></span>

<span data-ttu-id="02b67-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="02b67-115">The type of `array` elements.</span></span>