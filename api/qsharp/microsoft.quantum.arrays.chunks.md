---
uid: Microsoft.Quantum.Arrays.Chunks
title: Blöcke (Funktion)
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: fe10999d35ed05908fd59b9dad8b5c0c51233ae6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706175"
---
# <a name="chunks-function"></a><span data-ttu-id="a216f-102">Blöcke (Funktion)</span><span class="sxs-lookup"><span data-stu-id="a216f-102">Chunks function</span></span>

<span data-ttu-id="a216f-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a216f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a216f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a216f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a216f-105">Teilt ein Array in mehrere Teile der gleichen Länge.</span><span class="sxs-lookup"><span data-stu-id="a216f-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="a216f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a216f-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="a216f-107">nelements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a216f-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a216f-108">Die Länge der einzelnen Segmente.</span><span class="sxs-lookup"><span data-stu-id="a216f-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="a216f-109">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="a216f-109">arr : 'T[]</span></span>

<span data-ttu-id="a216f-110">Das Array, das aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a216f-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="a216f-111">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="a216f-111">Output : 'T[][]</span></span>

<span data-ttu-id="a216f-112">Ein-Array, das die einzelnen Segmente des ursprünglichen Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="a216f-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a216f-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a216f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a216f-114">GIF</span><span class="sxs-lookup"><span data-stu-id="a216f-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="a216f-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a216f-115">Remarks</span></span>

<span data-ttu-id="a216f-116">Beachten Sie, dass das letzte Element der Ausgabe möglicherweise kürzer `nElements` ist, als wenn `Length(arr)` von nicht teilbar ist `nElements` .</span><span class="sxs-lookup"><span data-stu-id="a216f-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>