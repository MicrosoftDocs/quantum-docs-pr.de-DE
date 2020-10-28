---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Entzippte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 37c960dc5dbdb8099fbebe1ad63cb44ce642733c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705722"
---
# <a name="unzipped-function"></a><span data-ttu-id="ce304-102">Entzippte Funktion</span><span class="sxs-lookup"><span data-stu-id="ce304-102">Unzipped function</span></span>

<span data-ttu-id="ce304-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ce304-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ce304-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ce304-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ce304-105">Gibt bei einem Array von 2-Tupeln ein Tupel mit zwei Arrays zurück, die jeweils die Elemente der Tupel des Eingabe Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="ce304-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="ce304-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce304-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="ce304-107">Arr: ('t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="ce304-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="ce304-108">Ein Array, das 2 Tupel enthält.</span><span class="sxs-lookup"><span data-stu-id="ce304-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="ce304-109">Ausgabe: ('t [], ' U [])</span><span class="sxs-lookup"><span data-stu-id="ce304-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="ce304-110">Zwei Arrays, das erste-Element, das alle ersten Elemente der eingabetupel enthält, das zweite Array, das alle zweiten Elemente der eingabentupel enthält.</span><span class="sxs-lookup"><span data-stu-id="ce304-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ce304-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ce304-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ce304-112">GIF</span><span class="sxs-lookup"><span data-stu-id="ce304-112">'T</span></span>

<span data-ttu-id="ce304-113">Der Typ des ersten Elements in jedem Tupel.</span><span class="sxs-lookup"><span data-stu-id="ce304-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="ce304-114">"U</span><span class="sxs-lookup"><span data-stu-id="ce304-114">'U</span></span>

<span data-ttu-id="ce304-115">Der Typ des zweiten Elements in jedem Tupel.</span><span class="sxs-lookup"><span data-stu-id="ce304-115">The type of the second element in each tuple</span></span>

## <a name="see-also"></a><span data-ttu-id="ce304-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ce304-116">See Also</span></span>

- [<span data-ttu-id="ce304-117">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="ce304-117">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)