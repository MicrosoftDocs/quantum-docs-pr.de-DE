---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Mappeer doverrange-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: e527a3ca1fd7571836f4f79bb453581f53d1db2b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705890"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="f1a9c-102">Mappeer doverrange-Funktion</span><span class="sxs-lookup"><span data-stu-id="f1a9c-102">MappedOverRange function</span></span>

<span data-ttu-id="f1a9c-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f1a9c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f1a9c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f1a9c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f1a9c-105">Gibt ein neues Array zurück, das aus den Bildern der Bereichs Werte unter der Funktion besteht, wenn ein Bereich und eine Funktion eine ganze Zahl als Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="f1a9c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f1a9c-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="f1a9c-107">Mapper: [int](xref:microsoft.quantum.lang-ref.int) -> 't</span><span class="sxs-lookup"><span data-stu-id="f1a9c-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="f1a9c-108">Eine Funktion von `Int` zu `'T` , die zum Zuordnen von Bereichs Werten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="f1a9c-109">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="f1a9c-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="f1a9c-110">Ein Bereich von ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="f1a9c-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="f1a9c-111">Output : 'T[]</span></span>

<span data-ttu-id="f1a9c-112">Ein Array `'T[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .</span><span class="sxs-lookup"><span data-stu-id="f1a9c-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f1a9c-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f1a9c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f1a9c-114">GIF</span><span class="sxs-lookup"><span data-stu-id="f1a9c-114">'T</span></span>

<span data-ttu-id="f1a9c-115">Der Ergebnistyp der `mapper` Funktion.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-115">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1a9c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f1a9c-116">Remarks</span></span>

<span data-ttu-id="f1a9c-117">Die-Funktion ist für generische Typen definiert, d. h., wenn wir über eine Funktion verfügen, `mapper: Int -> 'T` können wir die Werte des Bereichs zuordnen und ein Array vom Typ `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="f1a9c-117">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1a9c-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f1a9c-118">See Also</span></span>

- [<span data-ttu-id="f1a9c-119">Microsoft. Quantum. Arrays. zugeordnet</span><span class="sxs-lookup"><span data-stu-id="f1a9c-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)