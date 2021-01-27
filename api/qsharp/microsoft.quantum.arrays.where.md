---
uid: Microsoft.Quantum.Arrays.Where
title: Where-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 4a938114689177f7a9ee182e6e5f36debe4edac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842219"
---
# <a name="where-function"></a><span data-ttu-id="493d6-102">Where-Funktion</span><span class="sxs-lookup"><span data-stu-id="493d6-102">Where function</span></span>

<span data-ttu-id="493d6-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="493d6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="493d6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="493d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="493d6-105">Gibt bei Angabe eines Prädikats und eines Arrays die Indizes dieses Arrays zurück, bei denen das Prädikat "true" ist.</span><span class="sxs-lookup"><span data-stu-id="493d6-105">Given a predicate and an array, returns the indices of that array where the predicate is true.</span></span>

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="493d6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="493d6-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="493d6-107">Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="493d6-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="493d6-108">Eine Funktion von `'T` zu einem booleschen Wert, der zum Filtern von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="493d6-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="493d6-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="493d6-109">array : 'T[]</span></span>

<span data-ttu-id="493d6-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="493d6-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="493d6-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="493d6-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="493d6-112">Ein Array von Indizes, bei denen " `predicate` true" ist.</span><span class="sxs-lookup"><span data-stu-id="493d6-112">An array of indices where `predicate` is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="493d6-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="493d6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="493d6-114">GIF</span><span class="sxs-lookup"><span data-stu-id="493d6-114">'T</span></span>

<span data-ttu-id="493d6-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="493d6-115">The type of `array` elements.</span></span>