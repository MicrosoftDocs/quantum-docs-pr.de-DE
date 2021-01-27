---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Mappedbyindex-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 584cabcb7b6059ae5d311f13f5f75bd1f87bdba5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845662"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="e836b-102">Mappedbyindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="e836b-102">MappedByIndex function</span></span>

<span data-ttu-id="e836b-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e836b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e836b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e836b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e836b-105">Gibt ein neues Array zurück, das aus den Bildern des ursprünglichen Arrays unter der Funktion besteht, wenn ein Array und eine Funktion für die indizierten Elemente des Arrays definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e836b-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="e836b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e836b-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="e836b-107">Mapper: ([int](xref:microsoft.quantum.lang-ref.int), t)-> ' U</span><span class="sxs-lookup"><span data-stu-id="e836b-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="e836b-108">Eine Funktion von `(Int, 'T)` zu `'U` , die verwendet wird, um Elemente und ihre Indizes zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e836b-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="e836b-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="e836b-109">array : 'T[]</span></span>

<span data-ttu-id="e836b-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="e836b-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="e836b-111">Ausgabe: ' U []</span><span class="sxs-lookup"><span data-stu-id="e836b-111">Output : 'U[]</span></span>

<span data-ttu-id="e836b-112">Ein Array `'U[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .</span><span class="sxs-lookup"><span data-stu-id="e836b-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e836b-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e836b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e836b-114">GIF</span><span class="sxs-lookup"><span data-stu-id="e836b-114">'T</span></span>

<span data-ttu-id="e836b-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="e836b-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="e836b-116">"U</span><span class="sxs-lookup"><span data-stu-id="e836b-116">'U</span></span>

<span data-ttu-id="e836b-117">Der Ergebnistyp der `mapper` Funktion.</span><span class="sxs-lookup"><span data-stu-id="e836b-117">The result type of the `mapper` function.</span></span>

## <a name="example"></a><span data-ttu-id="e836b-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e836b-118">Example</span></span>

<span data-ttu-id="e836b-119">Die folgenden beiden Zeilen sind äquivalent:</span><span class="sxs-lookup"><span data-stu-id="e836b-119">The following two lines are equivalent:</span></span>

```qsharp
let arr = MapIndex(f, [x0, x1, x2]);
```

<span data-ttu-id="e836b-120">and</span><span class="sxs-lookup"><span data-stu-id="e836b-120">and</span></span>

```qsharp
let arr = [f(0, x0), f(1, x1), f(2, x2)];
```

## <a name="see-also"></a><span data-ttu-id="e836b-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e836b-121">See Also</span></span>

- [<span data-ttu-id="e836b-122">Microsoft. Quantum. Arrays. zugeordnet</span><span class="sxs-lookup"><span data-stu-id="e836b-122">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)