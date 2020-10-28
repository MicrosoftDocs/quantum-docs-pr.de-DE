---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Lexographiccomparison-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: f0b68974a0ea26907b58971e4fa4b1f06f5714d2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701441"
---
# <a name="lexographiccomparison-function"></a><span data-ttu-id="53939-102">Lexographiccomparison-Funktion</span><span class="sxs-lookup"><span data-stu-id="53939-102">LexographicComparison function</span></span>

<span data-ttu-id="53939-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="53939-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="53939-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="53939-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="53939-105">Gibt eine-Vergleichsfunktion zurück, die eine neue Funktion zurückgibt, die zwei Arrays lexografisch vergleicht.</span><span class="sxs-lookup"><span data-stu-id="53939-105">Given a comparison function, returns a new function that lexographically compares two arrays.</span></span>

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a><span data-ttu-id="53939-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53939-106">Input</span></span>

### <a name="elementcomparison--tt---bool"></a><span data-ttu-id="53939-107">Element Comparison: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="53939-107">elementComparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="53939-108">Eine Funktion, die zwei Elemente `x` und vergleicht und `y` zurückgibt, wenn `x` kleiner oder gleich ist `y` .</span><span class="sxs-lookup"><span data-stu-id="53939-108">A function that compares two elements `x` and `y` and returns if `x` is less than or equal to `y`.</span></span>



## <a name="output--tt---bool"></a><span data-ttu-id="53939-109">Ausgabe: ('t [], 't [])-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="53939-109">Output : ('T[],'T[]) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="53939-110">Eine Funktion, die zwei Arrays `xs` und vergleicht und `ys` zurückgibt, wenn `xs` vor oder gleich `ys` in der lexographical-Reihenfolge auftritt.</span><span class="sxs-lookup"><span data-stu-id="53939-110">A function that compares two arrays `xs` and `ys` and returns if `xs` occurs before or equal to `ys` in lexographical ordering.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="53939-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="53939-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="53939-112">GIF</span><span class="sxs-lookup"><span data-stu-id="53939-112">'T</span></span>

<span data-ttu-id="53939-113">Der Typ der Elemente der zu vergleichenden Arrays.</span><span class="sxs-lookup"><span data-stu-id="53939-113">The type of the elements of the arrays being compared.</span></span>

## <a name="remarks"></a><span data-ttu-id="53939-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53939-114">Remarks</span></span>

<span data-ttu-id="53939-115">Der lexografischen Vergleich zwischen zwei Arrays `xs` und `ys` wird durch die folgende Prozedur definiert.</span><span class="sxs-lookup"><span data-stu-id="53939-115">The lexographic comparison between two arrays `xs` and `ys` is defined by the following procedure.</span></span> <span data-ttu-id="53939-116">Wir sagen, dass zwei Elemente `x` und `y` äquivalent sind, wenn `elementComparison(x, y)` und beide "true" `elementComparison(y, x)` sind.</span><span class="sxs-lookup"><span data-stu-id="53939-116">We say that two elements `x` and `y` are equivalent if `elementComparison(x, y)` and `elementComparison(y, x)` are both true.</span></span>

- <span data-ttu-id="53939-117">Beide Arrays werden Element-für-Element-Elemente verglichen, bis das erste Paar Elemente, die nicht äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="53939-117">Both arrays are compared element-by-element until the first pair of elements that are not equivalent.</span></span> <span data-ttu-id="53939-118">Das Array, das das Element enthält, das zuerst anhand von auftritt, `elementComparison` wird als erstes in der lexographical-Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53939-118">The array containing the element that occurs first according to `elementComparison` is said to occur first in lexographical ordering.</span></span>
- <span data-ttu-id="53939-119">Wenn keine nicht gleichwertigen Elemente gefunden werden und ein Array länger als das andere ist, wird das kürzere Array als erstes Vorkommen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="53939-119">If no inequivalent elements are found, and one array is longer than the other, the shorter array is said to occur first.</span></span>

## <a name="see-also"></a><span data-ttu-id="53939-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53939-120">See Also</span></span>

- [<span data-ttu-id="53939-121">Microsoft. Quantum. Arrays. sortiert</span><span class="sxs-lookup"><span data-stu-id="53939-121">Microsoft.Quantum.Arrays.Sorted</span></span>](xref:Microsoft.Quantum.Arrays.Sorted)