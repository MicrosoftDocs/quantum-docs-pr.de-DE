---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Entzippte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 7eea7982721dc596b8660be5f3634df71b1ddf95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845379"
---
# <a name="unzipped-function"></a><span data-ttu-id="0b65b-102">Entzippte Funktion</span><span class="sxs-lookup"><span data-stu-id="0b65b-102">Unzipped function</span></span>

<span data-ttu-id="0b65b-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0b65b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0b65b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0b65b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0b65b-105">Gibt bei einem Array von 2-Tupeln ein Tupel mit zwei Arrays zurück, die jeweils die Elemente der Tupel des Eingabe Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b65b-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="0b65b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0b65b-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="0b65b-107">Arr: ('t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="0b65b-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="0b65b-108">Ein Array, das 2 Tupel enthält.</span><span class="sxs-lookup"><span data-stu-id="0b65b-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="0b65b-109">Ausgabe: ('t [], ' U [])</span><span class="sxs-lookup"><span data-stu-id="0b65b-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="0b65b-110">Zwei Arrays, das erste-Element, das alle ersten Elemente der eingabetupel enthält, das zweite Array, das alle zweiten Elemente der eingabentupel enthält.</span><span class="sxs-lookup"><span data-stu-id="0b65b-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0b65b-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="0b65b-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0b65b-112">GIF</span><span class="sxs-lookup"><span data-stu-id="0b65b-112">'T</span></span>

<span data-ttu-id="0b65b-113">Der Typ des ersten Elements in jedem Tupel.</span><span class="sxs-lookup"><span data-stu-id="0b65b-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="0b65b-114">"U</span><span class="sxs-lookup"><span data-stu-id="0b65b-114">'U</span></span>

<span data-ttu-id="0b65b-115">Der Typ des zweiten Elements in jedem Tupel.</span><span class="sxs-lookup"><span data-stu-id="0b65b-115">The type of the second element in each tuple</span></span>

## <a name="example"></a><span data-ttu-id="0b65b-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0b65b-116">Example</span></span>

```qsharp
// split is same as ([6, 5, 5, 3, 2, 1], [true, false, false, false, true, false])
let split = Unzipped([(6, true), (5, false), (5, false), (3, false), (2, true), (1, false)]);
```

## <a name="see-also"></a><span data-ttu-id="0b65b-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0b65b-117">See Also</span></span>

- [<span data-ttu-id="0b65b-118">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="0b65b-118">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)