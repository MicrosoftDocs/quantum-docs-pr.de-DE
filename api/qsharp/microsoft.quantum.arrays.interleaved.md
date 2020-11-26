---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220959"
---
# <a name="interleaved-function"></a><span data-ttu-id="30a9f-102">Interleaved-Funktion</span><span class="sxs-lookup"><span data-stu-id="30a9f-102">Interleaved function</span></span>

<span data-ttu-id="30a9f-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="30a9f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="30a9f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="30a9f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="30a9f-105">Interverlässt zwei Arrays von (fast) gleicher Größe.</span><span class="sxs-lookup"><span data-stu-id="30a9f-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="30a9f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30a9f-106">Description</span></span>

<span data-ttu-id="30a9f-107">Diese Funktion gibt die überlappenden von zwei Arrays zurück, beginnend mit dem ersten Element aus dem ersten Array, dann mit dem ersten Element aus dem zweiten Array usw.</span><span class="sxs-lookup"><span data-stu-id="30a9f-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="30a9f-108">Das erste Array muss entweder dieselbe Länge wie das zweite Array aufweisen, oder es kann ein einziges Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="30a9f-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="30a9f-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30a9f-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="30a9f-110">zuerst: 't []</span><span class="sxs-lookup"><span data-stu-id="30a9f-110">first : 'T[]</span></span>

<span data-ttu-id="30a9f-111">Das erste zu verschachtelende Array.</span><span class="sxs-lookup"><span data-stu-id="30a9f-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="30a9f-112">Sekunde: 't []</span><span class="sxs-lookup"><span data-stu-id="30a9f-112">second : 'T[]</span></span>

<span data-ttu-id="30a9f-113">Das zweite Array, das verschachtelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="30a9f-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="30a9f-114">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="30a9f-114">Output : 'T[]</span></span>

<span data-ttu-id="30a9f-115">Verschachtelte Arrays</span><span class="sxs-lookup"><span data-stu-id="30a9f-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="30a9f-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="30a9f-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="30a9f-117">GIF</span><span class="sxs-lookup"><span data-stu-id="30a9f-117">'T</span></span>

<span data-ttu-id="30a9f-118">Der Typ der einzelnen Elemente von `first` und `second` .</span><span class="sxs-lookup"><span data-stu-id="30a9f-118">The type of each element of `first` and `second`.</span></span>