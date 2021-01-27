---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 3605c0d0bc43cdb1097d025861c3ec2424763c86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848114"
---
# <a name="interleaved-function"></a><span data-ttu-id="dfcc0-102">Interleaved-Funktion</span><span class="sxs-lookup"><span data-stu-id="dfcc0-102">Interleaved function</span></span>

<span data-ttu-id="dfcc0-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dfcc0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dfcc0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dfcc0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dfcc0-105">Interverlässt zwei Arrays von (fast) gleicher Größe.</span><span class="sxs-lookup"><span data-stu-id="dfcc0-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="dfcc0-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfcc0-106">Description</span></span>

<span data-ttu-id="dfcc0-107">Diese Funktion gibt die überlappenden von zwei Arrays zurück, beginnend mit dem ersten Element aus dem ersten Array, dann mit dem ersten Element aus dem zweiten Array usw.</span><span class="sxs-lookup"><span data-stu-id="dfcc0-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="dfcc0-108">Das erste Array muss entweder dieselbe Länge wie das zweite Array aufweisen, oder es kann ein einziges Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dfcc0-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="dfcc0-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfcc0-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="dfcc0-110">zuerst: 't []</span><span class="sxs-lookup"><span data-stu-id="dfcc0-110">first : 'T[]</span></span>

<span data-ttu-id="dfcc0-111">Das erste zu verschachtelende Array.</span><span class="sxs-lookup"><span data-stu-id="dfcc0-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="dfcc0-112">Sekunde: 't []</span><span class="sxs-lookup"><span data-stu-id="dfcc0-112">second : 'T[]</span></span>

<span data-ttu-id="dfcc0-113">Das zweite Array, das verschachtelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dfcc0-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="dfcc0-114">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="dfcc0-114">Output : 'T[]</span></span>

<span data-ttu-id="dfcc0-115">Verschachtelte Arrays</span><span class="sxs-lookup"><span data-stu-id="dfcc0-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dfcc0-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="dfcc0-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dfcc0-117">GIF</span><span class="sxs-lookup"><span data-stu-id="dfcc0-117">'T</span></span>

<span data-ttu-id="dfcc0-118">Der Typ der einzelnen Elemente von `first` und `second` .</span><span class="sxs-lookup"><span data-stu-id="dfcc0-118">The type of each element of `first` and `second`.</span></span>

## <a name="example"></a><span data-ttu-id="dfcc0-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dfcc0-119">Example</span></span>

```qsharp
// same as int1 = [1, -1, 2, -2, 3, -3]
let int1 = Interleaved([1, 2, 3], [-1, -2, -3])

// same as int2 = [false, true, false, true, false]
let int2 = Interleaved(ConstantArray(3, false), ConstantArray(2, true));
```