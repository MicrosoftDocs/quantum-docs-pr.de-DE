---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Mappeer doverrange-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: b1d73c2503e63ed09a3d6a56421760ca29eb0c3f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220687"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="3ce49-102">Mappeer doverrange-Funktion</span><span class="sxs-lookup"><span data-stu-id="3ce49-102">MappedOverRange function</span></span>

<span data-ttu-id="3ce49-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3ce49-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3ce49-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3ce49-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3ce49-105">Gibt ein neues Array zurück, das aus den Bildern der Bereichs Werte unter der Funktion besteht, wenn ein Bereich und eine Funktion eine ganze Zahl als Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="3ce49-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="3ce49-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ce49-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="3ce49-107">Mapper: [int](xref:microsoft.quantum.lang-ref.int) -> 't</span><span class="sxs-lookup"><span data-stu-id="3ce49-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="3ce49-108">Eine Funktion von `Int` zu `'T` , die zum Zuordnen von Bereichs Werten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ce49-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="3ce49-109">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="3ce49-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="3ce49-110">Ein Bereich von ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="3ce49-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="3ce49-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="3ce49-111">Output : 'T[]</span></span>

<span data-ttu-id="3ce49-112">Ein Array `'T[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .</span><span class="sxs-lookup"><span data-stu-id="3ce49-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3ce49-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3ce49-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3ce49-114">GIF</span><span class="sxs-lookup"><span data-stu-id="3ce49-114">'T</span></span>

<span data-ttu-id="3ce49-115">Der Ergebnistyp der `mapper` Funktion.</span><span class="sxs-lookup"><span data-stu-id="3ce49-115">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ce49-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ce49-116">Remarks</span></span>

<span data-ttu-id="3ce49-117">Die-Funktion ist für generische Typen definiert, d. h., wenn wir über eine Funktion verfügen, `mapper: Int -> 'T` können wir die Werte des Bereichs zuordnen und ein Array vom Typ `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="3ce49-117">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ce49-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3ce49-118">See Also</span></span>

- [<span data-ttu-id="3ce49-119">Microsoft. Quantum. Arrays. zugeordnet</span><span class="sxs-lookup"><span data-stu-id="3ce49-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)