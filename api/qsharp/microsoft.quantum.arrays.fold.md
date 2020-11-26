---
uid: Microsoft.Quantum.Arrays.Fold
title: Fold-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: a42f9a832c18bd612c1ae416187f3f2513eed54d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221163"
---
# <a name="fold-function"></a><span data-ttu-id="a579e-102">Fold-Funktion</span><span class="sxs-lookup"><span data-stu-id="a579e-102">Fold function</span></span>

<span data-ttu-id="a579e-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a579e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a579e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a579e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a579e-105">Iteriert eine Funktion `f` durch ein Array `array` und gibt zurück `f(f(f(initialState, array[0]), array[1]), ...)` .</span><span class="sxs-lookup"><span data-stu-id="a579e-105">Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.</span></span>

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a><span data-ttu-id="a579e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a579e-106">Input</span></span>

### <a name="folder--statet---state"></a><span data-ttu-id="a579e-107">Ordner: (' State, 't)-> ' State</span><span class="sxs-lookup"><span data-stu-id="a579e-107">folder : ('State,'T) -> 'State</span></span>

<span data-ttu-id="a579e-108">Eine Funktion, die über das Array gefaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a579e-108">A function to be folded over the array.</span></span>


### <a name="state--state"></a><span data-ttu-id="a579e-109">Status: "State"</span><span class="sxs-lookup"><span data-stu-id="a579e-109">state : 'State</span></span>

<span data-ttu-id="a579e-110">Der anfängliche Zustand des Ordners.</span><span class="sxs-lookup"><span data-stu-id="a579e-110">The initial state of the folder.</span></span>


### <a name="array--t"></a><span data-ttu-id="a579e-111">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="a579e-111">array : 'T[]</span></span>

<span data-ttu-id="a579e-112">Ein Array von Werten, die zusammengeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a579e-112">An array of values to be folded over.</span></span>



## <a name="output--state"></a><span data-ttu-id="a579e-113">Ausgabe: "State</span><span class="sxs-lookup"><span data-stu-id="a579e-113">Output : 'State</span></span>

<span data-ttu-id="a579e-114">Der endgültige Zustand, der vom Ordner nach dem Durchlaufen aller Elemente von zurückgegeben wird `array` .</span><span class="sxs-lookup"><span data-stu-id="a579e-114">The final state returned by the folder after iterating over all elements of `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a579e-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a579e-115">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="a579e-116">"State"</span><span class="sxs-lookup"><span data-stu-id="a579e-116">'State</span></span>

<span data-ttu-id="a579e-117">Der Typ der Zustände `folder` , mit denen die Funktion arbeitet, d. h., akzeptiert als erstes Argument und gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="a579e-117">The type of states the `folder` function operates on, i.e., accepts as its first argument and returns.</span></span>
### <a name="t"></a><span data-ttu-id="a579e-118">GIF</span><span class="sxs-lookup"><span data-stu-id="a579e-118">'T</span></span>

<span data-ttu-id="a579e-119">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="a579e-119">The type of `array` elements.</span></span>