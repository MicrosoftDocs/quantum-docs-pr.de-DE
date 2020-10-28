---
uid: Microsoft.Quantum.Arrays.Mapped
title: Zugeordnete Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 1abb9d6fb1a921b49554bef968442f4f2b346b71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705914"
---
# <a name="mapped-function"></a><span data-ttu-id="51d98-102">Zugeordnete Funktion</span><span class="sxs-lookup"><span data-stu-id="51d98-102">Mapped function</span></span>

<span data-ttu-id="51d98-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="51d98-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="51d98-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51d98-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51d98-105">Bei Angabe eines Arrays und einer Funktion, die für die Elemente des Arrays definiert ist, wird ein neues Array zurückgegeben, das aus den Bildern des ursprünglichen Arrays unter der Funktion besteht.</span><span class="sxs-lookup"><span data-stu-id="51d98-105">Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="51d98-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="51d98-106">Input</span></span>

### <a name="mapper--t---u"></a><span data-ttu-id="51d98-107">Mapper: 't-> ' U</span><span class="sxs-lookup"><span data-stu-id="51d98-107">mapper : 'T -> 'U</span></span>

<span data-ttu-id="51d98-108">Eine Funktion von `'T` zu `'U` , die zum Zuordnen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51d98-108">A function from `'T` to `'U` that is used to map elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="51d98-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="51d98-109">array : 'T[]</span></span>

<span data-ttu-id="51d98-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="51d98-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="51d98-111">Ausgabe: ' U []</span><span class="sxs-lookup"><span data-stu-id="51d98-111">Output : 'U[]</span></span>

<span data-ttu-id="51d98-112">Ein Array `'U[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .</span><span class="sxs-lookup"><span data-stu-id="51d98-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="51d98-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="51d98-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="51d98-114">GIF</span><span class="sxs-lookup"><span data-stu-id="51d98-114">'T</span></span>

<span data-ttu-id="51d98-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="51d98-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="51d98-116">"U</span><span class="sxs-lookup"><span data-stu-id="51d98-116">'U</span></span>

<span data-ttu-id="51d98-117">Der Ergebnistyp der `mapper` Funktion.</span><span class="sxs-lookup"><span data-stu-id="51d98-117">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d98-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51d98-118">Remarks</span></span>

<span data-ttu-id="51d98-119">Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `mapper: 'T -> 'U` können wir die Elemente des Arrays zuordnen und ein neues Array vom Typ entwickeln `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="51d98-119">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `mapper: 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>