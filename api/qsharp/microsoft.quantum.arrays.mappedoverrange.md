---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Mappeer doverrange-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: 7093043e2a290e6132774b8fe154d3627a254f27
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845652"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="a5ba2-102">Mappeer doverrange-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5ba2-102">MappedOverRange function</span></span>

<span data-ttu-id="a5ba2-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a5ba2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a5ba2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a5ba2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a5ba2-105">Gibt ein neues Array zurück, das aus den Bildern der Bereichs Werte unter der Funktion besteht, wenn ein Bereich und eine Funktion eine ganze Zahl als Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="a5ba2-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="a5ba2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a5ba2-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="a5ba2-107">Mapper: [int](xref:microsoft.quantum.lang-ref.int) -> 't</span><span class="sxs-lookup"><span data-stu-id="a5ba2-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="a5ba2-108">Eine Funktion von `Int` zu `'T` , die zum Zuordnen von Bereichs Werten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5ba2-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="a5ba2-109">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="a5ba2-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="a5ba2-110">Ein Bereich von ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="a5ba2-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="a5ba2-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="a5ba2-111">Output : 'T[]</span></span>

<span data-ttu-id="a5ba2-112">Ein Array `'T[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .</span><span class="sxs-lookup"><span data-stu-id="a5ba2-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a5ba2-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a5ba2-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a5ba2-114">GIF</span><span class="sxs-lookup"><span data-stu-id="a5ba2-114">'T</span></span>

<span data-ttu-id="a5ba2-115">Der Ergebnistyp der `mapper` Funktion.</span><span class="sxs-lookup"><span data-stu-id="a5ba2-115">The result type of the `mapper` function.</span></span>

## <a name="example"></a><span data-ttu-id="a5ba2-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a5ba2-116">Example</span></span>

<span data-ttu-id="a5ba2-117">In diesem Beispiel wird 1 zu einem Bereich von geraden Zahlen addiert:</span><span class="sxs-lookup"><span data-stu-id="a5ba2-117">This example adds 1 to a range of even numbers:</span></span>

```qsharp
let numbers = MappedOverRange(PlusI(1, _), 0..2..10);
// numbers = [1, 3, 5, 7, 9, 11]
```

## <a name="remarks"></a><span data-ttu-id="a5ba2-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5ba2-118">Remarks</span></span>

<span data-ttu-id="a5ba2-119">Die-Funktion ist für generische Typen definiert, d. h., wenn wir über eine Funktion verfügen, `mapper: Int -> 'T` können wir die Werte des Bereichs zuordnen und ein Array vom Typ `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="a5ba2-119">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5ba2-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a5ba2-120">See Also</span></span>

- [<span data-ttu-id="a5ba2-121">Microsoft. Quantum. Arrays. zugeordnet</span><span class="sxs-lookup"><span data-stu-id="a5ba2-121">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)