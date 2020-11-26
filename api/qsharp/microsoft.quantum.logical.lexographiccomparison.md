---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Lexographiccomparison-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: 4d8596c52b0fc8082a2b766d95d4052a4964b8b9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197583"
---
# <a name="lexographiccomparison-function"></a><span data-ttu-id="c03d5-102">Lexographiccomparison-Funktion</span><span class="sxs-lookup"><span data-stu-id="c03d5-102">LexographicComparison function</span></span>

<span data-ttu-id="c03d5-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="c03d5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="c03d5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c03d5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c03d5-105">Gibt eine-Vergleichsfunktion zurück, die eine neue Funktion zurückgibt, die zwei Arrays lexografisch vergleicht.</span><span class="sxs-lookup"><span data-stu-id="c03d5-105">Given a comparison function, returns a new function that lexographically compares two arrays.</span></span>

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a><span data-ttu-id="c03d5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c03d5-106">Input</span></span>

### <a name="elementcomparison--tt---bool"></a><span data-ttu-id="c03d5-107">Element Comparison: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c03d5-107">elementComparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c03d5-108">Eine Funktion, die zwei Elemente `x` und vergleicht und `y` zurückgibt, wenn `x` kleiner oder gleich ist `y` .</span><span class="sxs-lookup"><span data-stu-id="c03d5-108">A function that compares two elements `x` and `y` and returns if `x` is less than or equal to `y`.</span></span>



## <a name="output--tt---bool"></a><span data-ttu-id="c03d5-109">Ausgabe: ('t [], 't [])-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c03d5-109">Output : ('T[],'T[]) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c03d5-110">Eine Funktion, die zwei Arrays `xs` und vergleicht und `ys` zurückgibt, wenn `xs` vor oder gleich `ys` in der lexographical-Reihenfolge auftritt.</span><span class="sxs-lookup"><span data-stu-id="c03d5-110">A function that compares two arrays `xs` and `ys` and returns if `xs` occurs before or equal to `ys` in lexographical ordering.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c03d5-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c03d5-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c03d5-112">GIF</span><span class="sxs-lookup"><span data-stu-id="c03d5-112">'T</span></span>

<span data-ttu-id="c03d5-113">Der Typ der Elemente der zu vergleichenden Arrays.</span><span class="sxs-lookup"><span data-stu-id="c03d5-113">The type of the elements of the arrays being compared.</span></span>

## <a name="remarks"></a><span data-ttu-id="c03d5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c03d5-114">Remarks</span></span>

<span data-ttu-id="c03d5-115">Der lexografischen Vergleich zwischen zwei Arrays `xs` und `ys` wird durch die folgende Prozedur definiert.</span><span class="sxs-lookup"><span data-stu-id="c03d5-115">The lexographic comparison between two arrays `xs` and `ys` is defined by the following procedure.</span></span> <span data-ttu-id="c03d5-116">Wir sagen, dass zwei Elemente `x` und `y` äquivalent sind, wenn `elementComparison(x, y)` und beide "true" `elementComparison(y, x)` sind.</span><span class="sxs-lookup"><span data-stu-id="c03d5-116">We say that two elements `x` and `y` are equivalent if `elementComparison(x, y)` and `elementComparison(y, x)` are both true.</span></span>

- <span data-ttu-id="c03d5-117">Beide Arrays werden Element-für-Element-Elemente verglichen, bis das erste Paar Elemente, die nicht äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="c03d5-117">Both arrays are compared element-by-element until the first pair of elements that are not equivalent.</span></span> <span data-ttu-id="c03d5-118">Das Array, das das Element enthält, das zuerst anhand von auftritt, `elementComparison` wird als erstes in der lexographical-Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c03d5-118">The array containing the element that occurs first according to `elementComparison` is said to occur first in lexographical ordering.</span></span>
- <span data-ttu-id="c03d5-119">Wenn keine nicht gleichwertigen Elemente gefunden werden und ein Array länger als das andere ist, wird das kürzere Array als erstes Vorkommen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c03d5-119">If no inequivalent elements are found, and one array is longer than the other, the shorter array is said to occur first.</span></span>

## <a name="see-also"></a><span data-ttu-id="c03d5-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c03d5-120">See Also</span></span>

- [<span data-ttu-id="c03d5-121">Microsoft. Quantum. Arrays. sortiert</span><span class="sxs-lookup"><span data-stu-id="c03d5-121">Microsoft.Quantum.Arrays.Sorted</span></span>](xref:Microsoft.Quantum.Arrays.Sorted)