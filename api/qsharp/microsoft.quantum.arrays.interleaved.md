---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 8405cabca17f2dd7c2680833bfab5c3768fcf752
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705959"
---
# <a name="interleaved-function"></a><span data-ttu-id="dd28a-102">Interleaved-Funktion</span><span class="sxs-lookup"><span data-stu-id="dd28a-102">Interleaved function</span></span>

<span data-ttu-id="dd28a-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dd28a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dd28a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dd28a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dd28a-105">Interverlässt zwei Arrays von (fast) gleicher Größe.</span><span class="sxs-lookup"><span data-stu-id="dd28a-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="dd28a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd28a-106">Description</span></span>

<span data-ttu-id="dd28a-107">Diese Funktion gibt die überlappenden von zwei Arrays zurück, beginnend mit dem ersten Element aus dem ersten Array, dann mit dem ersten Element aus dem zweiten Array usw.</span><span class="sxs-lookup"><span data-stu-id="dd28a-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="dd28a-108">Das erste Array muss entweder dieselbe Länge wie das zweite Array aufweisen, oder es kann ein einziges Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dd28a-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="dd28a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dd28a-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="dd28a-110">zuerst: 't []</span><span class="sxs-lookup"><span data-stu-id="dd28a-110">first : 'T[]</span></span>

<span data-ttu-id="dd28a-111">Das erste zu verschachtelende Array.</span><span class="sxs-lookup"><span data-stu-id="dd28a-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="dd28a-112">Sekunde: 't []</span><span class="sxs-lookup"><span data-stu-id="dd28a-112">second : 'T[]</span></span>

<span data-ttu-id="dd28a-113">Das zweite Array, das verschachtelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd28a-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="dd28a-114">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="dd28a-114">Output : 'T[]</span></span>

<span data-ttu-id="dd28a-115">Verschachtelte Arrays</span><span class="sxs-lookup"><span data-stu-id="dd28a-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dd28a-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="dd28a-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dd28a-117">GIF</span><span class="sxs-lookup"><span data-stu-id="dd28a-117">'T</span></span>

<span data-ttu-id="dd28a-118">Der Typ der einzelnen Elemente von `first` und `second` .</span><span class="sxs-lookup"><span data-stu-id="dd28a-118">The type of each element of `first` and `second`.</span></span>