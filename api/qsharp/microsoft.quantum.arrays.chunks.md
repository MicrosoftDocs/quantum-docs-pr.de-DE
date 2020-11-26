---
uid: Microsoft.Quantum.Arrays.Chunks
title: Blöcke (Funktion)
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: b323fdab1b207c72a4f46d5ca4cb368ecf0df818
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221605"
---
# <a name="chunks-function"></a><span data-ttu-id="c506e-102">Blöcke (Funktion)</span><span class="sxs-lookup"><span data-stu-id="c506e-102">Chunks function</span></span>

<span data-ttu-id="c506e-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c506e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c506e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c506e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c506e-105">Teilt ein Array in mehrere Teile der gleichen Länge.</span><span class="sxs-lookup"><span data-stu-id="c506e-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="c506e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c506e-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="c506e-107">nelements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c506e-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c506e-108">Die Länge der einzelnen Segmente.</span><span class="sxs-lookup"><span data-stu-id="c506e-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="c506e-109">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="c506e-109">arr : 'T[]</span></span>

<span data-ttu-id="c506e-110">Das Array, das aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c506e-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="c506e-111">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="c506e-111">Output : 'T[][]</span></span>

<span data-ttu-id="c506e-112">Ein-Array, das die einzelnen Segmente des ursprünglichen Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="c506e-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c506e-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c506e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c506e-114">GIF</span><span class="sxs-lookup"><span data-stu-id="c506e-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="c506e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c506e-115">Remarks</span></span>

<span data-ttu-id="c506e-116">Beachten Sie, dass das letzte Element der Ausgabe möglicherweise kürzer `nElements` ist, als wenn `Length(arr)` von nicht teilbar ist `nElements` .</span><span class="sxs-lookup"><span data-stu-id="c506e-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>