---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Kumuativegefaltete Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: a09c2779c8f06d8f6b7b0902366f3cefbbca4525
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706127"
---
# <a name="cumulativefolded-function"></a><span data-ttu-id="84864-102">Kumuativegefaltete Funktion</span><span class="sxs-lookup"><span data-stu-id="84864-102">CumulativeFolded function</span></span>

<span data-ttu-id="84864-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="84864-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="84864-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="84864-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="84864-105">Kombiniert zugeordnete und Fold in einer einzelnen Funktion</span><span class="sxs-lookup"><span data-stu-id="84864-105">Combines Mapped and Fold into a single function</span></span>

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a><span data-ttu-id="84864-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84864-106">Description</span></span>

<span data-ttu-id="84864-107">Diese Funktion durchläuft die `fn` Funktion durch das Array, beginnend bei einem Anfangszustand `state` und gibt alle Zwischenwerte zurück, ohne den Anfangszustand.</span><span class="sxs-lookup"><span data-stu-id="84864-107">This function iterates the `fn` function through the array, starting from an initial state `state` and returns all intermediate values, not including the inital state.</span></span>

## <a name="input"></a><span data-ttu-id="84864-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84864-108">Input</span></span>

### <a name="fn--statet---state"></a><span data-ttu-id="84864-109">FN: (' State, 't)-> ' State</span><span class="sxs-lookup"><span data-stu-id="84864-109">fn : ('State,'T) -> 'State</span></span>

<span data-ttu-id="84864-110">Eine Funktion, die über das Array gefaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="84864-110">A function to be folded over the array</span></span>


### <a name="state--state"></a><span data-ttu-id="84864-111">Status: "State"</span><span class="sxs-lookup"><span data-stu-id="84864-111">state : 'State</span></span>

<span data-ttu-id="84864-112">Der anfängliche Zustand, der gefaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="84864-112">The initial state to be folded</span></span>


### <a name="array--t"></a><span data-ttu-id="84864-113">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="84864-113">array : 'T[]</span></span>

<span data-ttu-id="84864-114">Ein Array von Werten, die zusammengeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="84864-114">An array of values to be folded over</span></span>



## <a name="output--state"></a><span data-ttu-id="84864-115">Ausgabe: ' State []</span><span class="sxs-lookup"><span data-stu-id="84864-115">Output : 'State[]</span></span>

<span data-ttu-id="84864-116">Alle Zwischenzustände, einschließlich des Endzustands, jedoch nicht der Anfangszustand.</span><span class="sxs-lookup"><span data-stu-id="84864-116">All intermediate states, including the final state, but not the initial state.</span></span>
<span data-ttu-id="84864-117">Die Länge des Ausgabe Arrays hat dieselbe Länge wie `array` .</span><span class="sxs-lookup"><span data-stu-id="84864-117">The length of the output array is of the same length as `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="84864-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="84864-118">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="84864-119">"State"</span><span class="sxs-lookup"><span data-stu-id="84864-119">'State</span></span>

<span data-ttu-id="84864-120">Der Typ der Zustände, mit denen die `fn` Funktion arbeitet, d. h., akzeptiert als erste Eingabe und gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="84864-120">The type of states that the `fn` function operates on, i.e., accepts as its first input and returns.</span></span>
### <a name="t"></a><span data-ttu-id="84864-121">GIF</span><span class="sxs-lookup"><span data-stu-id="84864-121">'T</span></span>

<span data-ttu-id="84864-122">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="84864-122">The type of `array` elements.</span></span>