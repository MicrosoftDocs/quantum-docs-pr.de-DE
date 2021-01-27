---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Kumuativegefaltete Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: 95cd5233a09a1234bba4de9fe870b9d93c0f86a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846246"
---
# <a name="cumulativefolded-function"></a><span data-ttu-id="1c318-102">Kumuativegefaltete Funktion</span><span class="sxs-lookup"><span data-stu-id="1c318-102">CumulativeFolded function</span></span>

<span data-ttu-id="1c318-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1c318-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1c318-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1c318-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1c318-105">Kombiniert zugeordnete und Fold in einer einzelnen Funktion</span><span class="sxs-lookup"><span data-stu-id="1c318-105">Combines Mapped and Fold into a single function</span></span>

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a><span data-ttu-id="1c318-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c318-106">Description</span></span>

<span data-ttu-id="1c318-107">Diese Funktion durchläuft die `fn` Funktion durch das Array, beginnend bei einem Anfangszustand `state` und gibt alle Zwischenwerte zurück, ohne den Anfangszustand.</span><span class="sxs-lookup"><span data-stu-id="1c318-107">This function iterates the `fn` function through the array, starting from an initial state `state` and returns all intermediate values, not including the inital state.</span></span>

## <a name="input"></a><span data-ttu-id="1c318-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1c318-108">Input</span></span>

### <a name="fn--statet---state"></a><span data-ttu-id="1c318-109">FN: (' State, 't)-> ' State</span><span class="sxs-lookup"><span data-stu-id="1c318-109">fn : ('State,'T) -> 'State</span></span>

<span data-ttu-id="1c318-110">Eine Funktion, die über das Array gefaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c318-110">A function to be folded over the array</span></span>


### <a name="state--state"></a><span data-ttu-id="1c318-111">Status: "State"</span><span class="sxs-lookup"><span data-stu-id="1c318-111">state : 'State</span></span>

<span data-ttu-id="1c318-112">Der anfängliche Zustand, der gefaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c318-112">The initial state to be folded</span></span>


### <a name="array--t"></a><span data-ttu-id="1c318-113">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="1c318-113">array : 'T[]</span></span>

<span data-ttu-id="1c318-114">Ein Array von Werten, die zusammengeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1c318-114">An array of values to be folded over</span></span>



## <a name="output--state"></a><span data-ttu-id="1c318-115">Ausgabe: ' State []</span><span class="sxs-lookup"><span data-stu-id="1c318-115">Output : 'State[]</span></span>

<span data-ttu-id="1c318-116">Alle Zwischenzustände, einschließlich des Endzustands, jedoch nicht der Anfangszustand.</span><span class="sxs-lookup"><span data-stu-id="1c318-116">All intermediate states, including the final state, but not the initial state.</span></span>
<span data-ttu-id="1c318-117">Die Länge des Ausgabe Arrays hat dieselbe Länge wie `array` .</span><span class="sxs-lookup"><span data-stu-id="1c318-117">The length of the output array is of the same length as `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1c318-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1c318-118">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="1c318-119">"State"</span><span class="sxs-lookup"><span data-stu-id="1c318-119">'State</span></span>

<span data-ttu-id="1c318-120">Der Typ der Zustände, mit denen die `fn` Funktion arbeitet, d. h., akzeptiert als erste Eingabe und gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="1c318-120">The type of states that the `fn` function operates on, i.e., accepts as its first input and returns.</span></span>
### <a name="t"></a><span data-ttu-id="1c318-121">GIF</span><span class="sxs-lookup"><span data-stu-id="1c318-121">'T</span></span>

<span data-ttu-id="1c318-122">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="1c318-122">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="1c318-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1c318-123">Example</span></span>

```qsharp
// same as sums = [1, 3, 6, 10, 15]
let sums = CumulativeFolded(PlusI, 0, SequenceI(1, 5));
```