---
uid: Microsoft.Quantum.Arrays.Chunks
title: Blöcke (Funktion)
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: 977594839a7d2fe09de8138d32a4a50e8a752390
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842871"
---
# <a name="chunks-function"></a><span data-ttu-id="64535-102">Blöcke (Funktion)</span><span class="sxs-lookup"><span data-stu-id="64535-102">Chunks function</span></span>

<span data-ttu-id="64535-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="64535-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="64535-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64535-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64535-105">Teilt ein Array in mehrere Teile der gleichen Länge.</span><span class="sxs-lookup"><span data-stu-id="64535-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="64535-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64535-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="64535-107">nelements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="64535-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="64535-108">Die Länge der einzelnen Segmente.</span><span class="sxs-lookup"><span data-stu-id="64535-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="64535-109">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="64535-109">arr : 'T[]</span></span>

<span data-ttu-id="64535-110">Das Array, das aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64535-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="64535-111">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="64535-111">Output : 'T[][]</span></span>

<span data-ttu-id="64535-112">Ein-Array, das die einzelnen Segmente des ursprünglichen Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="64535-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="64535-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="64535-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="64535-114">GIF</span><span class="sxs-lookup"><span data-stu-id="64535-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="64535-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64535-115">Remarks</span></span>

<span data-ttu-id="64535-116">Beachten Sie, dass das letzte Element der Ausgabe möglicherweise kürzer `nElements` ist, als wenn `Length(arr)` von nicht teilbar ist `nElements` .</span><span class="sxs-lookup"><span data-stu-id="64535-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>