---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Mappedbyindex-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 430495517974b641c249fa146aa9effec542e825
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209926"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="1dfa0-102">Mappedbyindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="1dfa0-102">MappedByIndex function</span></span>

<span data-ttu-id="1dfa0-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1dfa0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1dfa0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1dfa0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1dfa0-105">Gibt ein neues Array zurück, das aus den Bildern des ursprünglichen Arrays unter der Funktion besteht, wenn ein Array und eine Funktion für die indizierten Elemente des Arrays definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1dfa0-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="1dfa0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1dfa0-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="1dfa0-107">Mapper: ([int](xref:microsoft.quantum.lang-ref.int), t)-> ' U</span><span class="sxs-lookup"><span data-stu-id="1dfa0-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="1dfa0-108">Eine Funktion von `(Int, 'T)` zu `'U` , die verwendet wird, um Elemente und ihre Indizes zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="1dfa0-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="1dfa0-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="1dfa0-109">array : 'T[]</span></span>

<span data-ttu-id="1dfa0-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="1dfa0-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="1dfa0-111">Ausgabe: ' U []</span><span class="sxs-lookup"><span data-stu-id="1dfa0-111">Output : 'U[]</span></span>

<span data-ttu-id="1dfa0-112">Ein Array `'U[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .</span><span class="sxs-lookup"><span data-stu-id="1dfa0-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1dfa0-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1dfa0-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1dfa0-114">GIF</span><span class="sxs-lookup"><span data-stu-id="1dfa0-114">'T</span></span>

<span data-ttu-id="1dfa0-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="1dfa0-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="1dfa0-116">"U</span><span class="sxs-lookup"><span data-stu-id="1dfa0-116">'U</span></span>

<span data-ttu-id="1dfa0-117">Der Ergebnistyp der `mapper` Funktion.</span><span class="sxs-lookup"><span data-stu-id="1dfa0-117">The result type of the `mapper` function.</span></span>

## <a name="see-also"></a><span data-ttu-id="1dfa0-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1dfa0-118">See Also</span></span>

- [<span data-ttu-id="1dfa0-119">Microsoft. Quantum. Arrays. zugeordnet</span><span class="sxs-lookup"><span data-stu-id="1dfa0-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)