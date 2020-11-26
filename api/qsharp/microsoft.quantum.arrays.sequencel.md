---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequencel-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3e5c7f64825f09d82792d3e46fe3f53f5814510b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220262"
---
# <a name="sequencel-function"></a><span data-ttu-id="e4ec4-102">Sequencel-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4ec4-102">SequenceL function</span></span>

<span data-ttu-id="e4ec4-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e4ec4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e4ec4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e4ec4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e4ec4-105">Ein Array von ganzen Zahlen in einem angegebenen Intervall erhalten.</span><span class="sxs-lookup"><span data-stu-id="e4ec4-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="e4ec4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e4ec4-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="e4ec4-107">von: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="e4ec4-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="e4ec4-108">Ein inklusiver Start Index des Intervalls.</span><span class="sxs-lookup"><span data-stu-id="e4ec4-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="e4ec4-109">an: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="e4ec4-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="e4ec4-110">Ein inklusiver Endindex des Intervalls, das nicht kleiner als ist `from` .</span><span class="sxs-lookup"><span data-stu-id="e4ec4-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="e4ec4-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="e4ec4-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="e4ec4-112">Ein Array, das die Reihenfolge der Zahlen `from` , `from + 1` ,..., enthält `to` .</span><span class="sxs-lookup"><span data-stu-id="e4ec4-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4ec4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4ec4-113">Remarks</span></span>

<span data-ttu-id="e4ec4-114">Der Unterschied zwischen `from` und `to` muss in einen- `Int` Wert passen.</span><span class="sxs-lookup"><span data-stu-id="e4ec4-114">The difference between `from` and `to` must fit into an `Int` value.</span></span>