---
uid: Microsoft.Quantum.Arrays.Zipped
title: ZIP-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 56ed97d573bf29dddb7cdb1c3f360218bf97889a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219752"
---
# <a name="zipped-function"></a><span data-ttu-id="2f1b4-102">ZIP-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f1b4-102">Zipped function</span></span>

<span data-ttu-id="2f1b4-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2f1b4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2f1b4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2f1b4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2f1b4-105">Bei zwei Arrays wird ein neues Array von Paaren zurückgegeben, sodass jedes Paar ein Element aus jedem ursprünglichen Array enthält.</span><span class="sxs-lookup"><span data-stu-id="2f1b4-105">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="2f1b4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2f1b4-106">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="2f1b4-107">Left: 't []</span><span class="sxs-lookup"><span data-stu-id="2f1b4-107">left : 'T[]</span></span>

<span data-ttu-id="2f1b4-108">Ein Array, das Werte für das erste Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="2f1b4-108">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="2f1b4-109">Right: ' U []</span><span class="sxs-lookup"><span data-stu-id="2f1b4-109">right : 'U[]</span></span>

<span data-ttu-id="2f1b4-110">Ein Array, das Werte für das zweite Element jedes Tupels enthält.</span><span class="sxs-lookup"><span data-stu-id="2f1b4-110">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="2f1b4-111">Ausgabe: ('t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="2f1b4-111">Output : ('T,'U)[]</span></span>

<span data-ttu-id="2f1b4-112">Ein Array, das Paare des Formulars `(left[idx], right[idx])` für jedes enthält `idx` .</span><span class="sxs-lookup"><span data-stu-id="2f1b4-112">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="2f1b4-113">Wenn die beiden Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2f1b4-113">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2f1b4-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2f1b4-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2f1b4-115">GIF</span><span class="sxs-lookup"><span data-stu-id="2f1b4-115">'T</span></span>

<span data-ttu-id="2f1b4-116">Der Typ der linken Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="2f1b4-116">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="2f1b4-117">"U</span><span class="sxs-lookup"><span data-stu-id="2f1b4-117">'U</span></span>

<span data-ttu-id="2f1b4-118">Der Typ der rechten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="2f1b4-118">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f1b4-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f1b4-119">See Also</span></span>

- [<span data-ttu-id="2f1b4-120">Microsoft.Quantum.Arrays.ZipPED3</span><span class="sxs-lookup"><span data-stu-id="2f1b4-120">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)
- [<span data-ttu-id="2f1b4-121">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="2f1b4-121">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)
- [<span data-ttu-id="2f1b4-122">Microsoft. Quantum. Arrays. entzippt</span><span class="sxs-lookup"><span data-stu-id="2f1b4-122">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)