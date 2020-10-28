---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Mappedbyindex-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 07ca523248c363f2229551a14e77803dc4f4f82e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705898"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="2a2ca-102">Mappedbyindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="2a2ca-102">MappedByIndex function</span></span>

<span data-ttu-id="2a2ca-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2a2ca-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2a2ca-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a2ca-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2a2ca-105">Gibt ein neues Array zurück, das aus den Bildern des ursprünglichen Arrays unter der Funktion besteht, wenn ein Array und eine Funktion für die indizierten Elemente des Arrays definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2a2ca-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="2a2ca-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a2ca-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="2a2ca-107">Mapper: ([int](xref:microsoft.quantum.lang-ref.int), t)-> ' U</span><span class="sxs-lookup"><span data-stu-id="2a2ca-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="2a2ca-108">Eine Funktion von `(Int, 'T)` zu `'U` , die verwendet wird, um Elemente und ihre Indizes zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2a2ca-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="2a2ca-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="2a2ca-109">array : 'T[]</span></span>

<span data-ttu-id="2a2ca-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="2a2ca-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="2a2ca-111">Ausgabe: ' U []</span><span class="sxs-lookup"><span data-stu-id="2a2ca-111">Output : 'U[]</span></span>

<span data-ttu-id="2a2ca-112">Ein Array `'U[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .</span><span class="sxs-lookup"><span data-stu-id="2a2ca-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2a2ca-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2a2ca-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2a2ca-114">GIF</span><span class="sxs-lookup"><span data-stu-id="2a2ca-114">'T</span></span>

<span data-ttu-id="2a2ca-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="2a2ca-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="2a2ca-116">"U</span><span class="sxs-lookup"><span data-stu-id="2a2ca-116">'U</span></span>

<span data-ttu-id="2a2ca-117">Der Ergebnistyp der `mapper` Funktion.</span><span class="sxs-lookup"><span data-stu-id="2a2ca-117">The result type of the `mapper` function.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a2ca-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2a2ca-118">See Also</span></span>

- [<span data-ttu-id="2a2ca-119">Microsoft. Quantum. Arrays. zugeordnet</span><span class="sxs-lookup"><span data-stu-id="2a2ca-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)