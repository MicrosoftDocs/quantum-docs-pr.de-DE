---
uid: Microsoft.Quantum.Arrays.Fold
title: Fold-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: 47c23dd657391d80fe473d98f2036d8ddf1dbb0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706002"
---
# <a name="fold-function"></a><span data-ttu-id="f9546-102">Fold-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9546-102">Fold function</span></span>

<span data-ttu-id="f9546-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f9546-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f9546-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f9546-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f9546-105">Iteriert eine Funktion `f` durch ein Array `array` und gibt zurück `f(f(f(initialState, array[0]), array[1]), ...)` .</span><span class="sxs-lookup"><span data-stu-id="f9546-105">Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.</span></span>

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a><span data-ttu-id="f9546-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f9546-106">Input</span></span>

### <a name="folder--statet---state"></a><span data-ttu-id="f9546-107">Ordner: (' State, 't)-> ' State</span><span class="sxs-lookup"><span data-stu-id="f9546-107">folder : ('State,'T) -> 'State</span></span>

<span data-ttu-id="f9546-108">Eine Funktion, die über das Array gefaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9546-108">A function to be folded over the array.</span></span>


### <a name="state--state"></a><span data-ttu-id="f9546-109">Status: "State"</span><span class="sxs-lookup"><span data-stu-id="f9546-109">state : 'State</span></span>

<span data-ttu-id="f9546-110">Der anfängliche Zustand des Ordners.</span><span class="sxs-lookup"><span data-stu-id="f9546-110">The initial state of the folder.</span></span>


### <a name="array--t"></a><span data-ttu-id="f9546-111">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="f9546-111">array : 'T[]</span></span>

<span data-ttu-id="f9546-112">Ein Array von Werten, die zusammengeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f9546-112">An array of values to be folded over.</span></span>



## <a name="output--state"></a><span data-ttu-id="f9546-113">Ausgabe: "State</span><span class="sxs-lookup"><span data-stu-id="f9546-113">Output : 'State</span></span>

<span data-ttu-id="f9546-114">Der endgültige Zustand, der vom Ordner nach dem Durchlaufen aller Elemente von zurückgegeben wird `array` .</span><span class="sxs-lookup"><span data-stu-id="f9546-114">The final state returned by the folder after iterating over all elements of `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f9546-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f9546-115">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="f9546-116">"State"</span><span class="sxs-lookup"><span data-stu-id="f9546-116">'State</span></span>

<span data-ttu-id="f9546-117">Der Typ der Zustände `folder` , mit denen die Funktion arbeitet, d. h., akzeptiert als erstes Argument und gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="f9546-117">The type of states the `folder` function operates on, i.e., accepts as its first argument and returns.</span></span>
### <a name="t"></a><span data-ttu-id="f9546-118">GIF</span><span class="sxs-lookup"><span data-stu-id="f9546-118">'T</span></span>

<span data-ttu-id="f9546-119">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="f9546-119">The type of `array` elements.</span></span>