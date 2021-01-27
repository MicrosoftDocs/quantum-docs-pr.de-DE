---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Lexographiccomparison-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: de8179ab6e835d08e7f41287f31a876b7ecc91c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814379"
---
# <a name="lexographiccomparison-function"></a><span data-ttu-id="67c3c-102">Lexographiccomparison-Funktion</span><span class="sxs-lookup"><span data-stu-id="67c3c-102">LexographicComparison function</span></span>

<span data-ttu-id="67c3c-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="67c3c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="67c3c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="67c3c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="67c3c-105">Gibt eine-Vergleichsfunktion zurück, die eine neue Funktion zurückgibt, die zwei Arrays lexografisch vergleicht.</span><span class="sxs-lookup"><span data-stu-id="67c3c-105">Given a comparison function, returns a new function that lexographically compares two arrays.</span></span>

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a><span data-ttu-id="67c3c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="67c3c-106">Input</span></span>

### <a name="elementcomparison--tt---bool"></a><span data-ttu-id="67c3c-107">Element Comparison: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="67c3c-107">elementComparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="67c3c-108">Eine Funktion, die zwei Elemente `x` und vergleicht und `y` zurückgibt, wenn `x` kleiner oder gleich ist `y` .</span><span class="sxs-lookup"><span data-stu-id="67c3c-108">A function that compares two elements `x` and `y` and returns if `x` is less than or equal to `y`.</span></span>



## <a name="output--tt---bool"></a><span data-ttu-id="67c3c-109">Ausgabe: ('t [], 't [])-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="67c3c-109">Output : ('T[],'T[]) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="67c3c-110">Eine Funktion, die zwei Arrays `xs` und vergleicht und `ys` zurückgibt, wenn `xs` vor oder gleich `ys` in der lexographical-Reihenfolge auftritt.</span><span class="sxs-lookup"><span data-stu-id="67c3c-110">A function that compares two arrays `xs` and `ys` and returns if `xs` occurs before or equal to `ys` in lexographical ordering.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="67c3c-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="67c3c-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="67c3c-112">GIF</span><span class="sxs-lookup"><span data-stu-id="67c3c-112">'T</span></span>

<span data-ttu-id="67c3c-113">Der Typ der Elemente der zu vergleichenden Arrays.</span><span class="sxs-lookup"><span data-stu-id="67c3c-113">The type of the elements of the arrays being compared.</span></span>

## <a name="remarks"></a><span data-ttu-id="67c3c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67c3c-114">Remarks</span></span>

<span data-ttu-id="67c3c-115">Der lexografischen Vergleich zwischen zwei Arrays `xs` und `ys` wird durch die folgende Prozedur definiert.</span><span class="sxs-lookup"><span data-stu-id="67c3c-115">The lexographic comparison between two arrays `xs` and `ys` is defined by the following procedure.</span></span> <span data-ttu-id="67c3c-116">Wir sagen, dass zwei Elemente `x` und `y` äquivalent sind, wenn `elementComparison(x, y)` und beide "true" `elementComparison(y, x)` sind.</span><span class="sxs-lookup"><span data-stu-id="67c3c-116">We say that two elements `x` and `y` are equivalent if `elementComparison(x, y)` and `elementComparison(y, x)` are both true.</span></span>

- <span data-ttu-id="67c3c-117">Beide Arrays werden Element-für-Element-Elemente verglichen, bis das erste Paar Elemente, die nicht äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="67c3c-117">Both arrays are compared element-by-element until the first pair of elements that are not equivalent.</span></span> <span data-ttu-id="67c3c-118">Das Array, das das Element enthält, das zuerst anhand von auftritt, `elementComparison` wird als erstes in der lexographical-Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="67c3c-118">The array containing the element that occurs first according to `elementComparison` is said to occur first in lexographical ordering.</span></span>
- <span data-ttu-id="67c3c-119">Wenn keine nicht gleichwertigen Elemente gefunden werden und ein Array länger als das andere ist, wird das kürzere Array als erstes Vorkommen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="67c3c-119">If no inequivalent elements are found, and one array is longer than the other, the shorter array is said to occur first.</span></span>

## <a name="see-also"></a><span data-ttu-id="67c3c-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="67c3c-120">See Also</span></span>

- [<span data-ttu-id="67c3c-121">Microsoft. Quantum. Arrays. sortiert</span><span class="sxs-lookup"><span data-stu-id="67c3c-121">Microsoft.Quantum.Arrays.Sorted</span></span>](xref:Microsoft.Quantum.Arrays.Sorted)