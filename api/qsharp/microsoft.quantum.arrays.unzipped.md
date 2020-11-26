---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Entzippte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: aee1d48c9e0a1f104040bc56c78fdbb8bc4d34ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219956"
---
# <a name="unzipped-function"></a><span data-ttu-id="324ca-102">Entzippte Funktion</span><span class="sxs-lookup"><span data-stu-id="324ca-102">Unzipped function</span></span>

<span data-ttu-id="324ca-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="324ca-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="324ca-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="324ca-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="324ca-105">Gibt bei einem Array von 2-Tupeln ein Tupel mit zwei Arrays zurück, die jeweils die Elemente der Tupel des Eingabe Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="324ca-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="324ca-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="324ca-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="324ca-107">Arr: ('t, ' U) []</span><span class="sxs-lookup"><span data-stu-id="324ca-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="324ca-108">Ein Array, das 2 Tupel enthält.</span><span class="sxs-lookup"><span data-stu-id="324ca-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="324ca-109">Ausgabe: ('t [], ' U [])</span><span class="sxs-lookup"><span data-stu-id="324ca-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="324ca-110">Zwei Arrays, das erste-Element, das alle ersten Elemente der eingabetupel enthält, das zweite Array, das alle zweiten Elemente der eingabentupel enthält.</span><span class="sxs-lookup"><span data-stu-id="324ca-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="324ca-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="324ca-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="324ca-112">GIF</span><span class="sxs-lookup"><span data-stu-id="324ca-112">'T</span></span>

<span data-ttu-id="324ca-113">Der Typ des ersten Elements in jedem Tupel.</span><span class="sxs-lookup"><span data-stu-id="324ca-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="324ca-114">"U</span><span class="sxs-lookup"><span data-stu-id="324ca-114">'U</span></span>

<span data-ttu-id="324ca-115">Der Typ des zweiten Elements in jedem Tupel.</span><span class="sxs-lookup"><span data-stu-id="324ca-115">The type of the second element in each tuple</span></span>

## <a name="see-also"></a><span data-ttu-id="324ca-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="324ca-116">See Also</span></span>

- [<span data-ttu-id="324ca-117">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="324ca-117">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)