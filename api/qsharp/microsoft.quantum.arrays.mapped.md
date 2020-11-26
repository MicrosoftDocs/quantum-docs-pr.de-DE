---
uid: Microsoft.Quantum.Arrays.Mapped
title: Zugeordnete Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 9632b9f53ffad8ece958ab1dc9ad446c7dcb9e13
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220738"
---
# <a name="mapped-function"></a><span data-ttu-id="96d7c-102">Zugeordnete Funktion</span><span class="sxs-lookup"><span data-stu-id="96d7c-102">Mapped function</span></span>

<span data-ttu-id="96d7c-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="96d7c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="96d7c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="96d7c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="96d7c-105">Bei Angabe eines Arrays und einer Funktion, die für die Elemente des Arrays definiert ist, wird ein neues Array zurückgegeben, das aus den Bildern des ursprünglichen Arrays unter der Funktion besteht.</span><span class="sxs-lookup"><span data-stu-id="96d7c-105">Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="96d7c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96d7c-106">Input</span></span>

### <a name="mapper--t---u"></a><span data-ttu-id="96d7c-107">Mapper: 't-> ' U</span><span class="sxs-lookup"><span data-stu-id="96d7c-107">mapper : 'T -> 'U</span></span>

<span data-ttu-id="96d7c-108">Eine Funktion von `'T` zu `'U` , die zum Zuordnen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96d7c-108">A function from `'T` to `'U` that is used to map elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="96d7c-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="96d7c-109">array : 'T[]</span></span>

<span data-ttu-id="96d7c-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="96d7c-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="96d7c-111">Ausgabe: ' U []</span><span class="sxs-lookup"><span data-stu-id="96d7c-111">Output : 'U[]</span></span>

<span data-ttu-id="96d7c-112">Ein Array `'U[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .</span><span class="sxs-lookup"><span data-stu-id="96d7c-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="96d7c-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="96d7c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="96d7c-114">GIF</span><span class="sxs-lookup"><span data-stu-id="96d7c-114">'T</span></span>

<span data-ttu-id="96d7c-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="96d7c-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="96d7c-116">"U</span><span class="sxs-lookup"><span data-stu-id="96d7c-116">'U</span></span>

<span data-ttu-id="96d7c-117">Der Ergebnistyp der `mapper` Funktion.</span><span class="sxs-lookup"><span data-stu-id="96d7c-117">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="96d7c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96d7c-118">Remarks</span></span>

<span data-ttu-id="96d7c-119">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `mapper: 'T -> 'U` können wir die Elemente des Arrays zuordnen und ein neues Array vom Typ entwickeln `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="96d7c-119">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `mapper: 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>