---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequencel-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5ce63575e703341fce42c0be393765c342bbd89
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705783"
---
# <a name="sequencel-function"></a><span data-ttu-id="547d5-102">Sequencel-Funktion</span><span class="sxs-lookup"><span data-stu-id="547d5-102">SequenceL function</span></span>

<span data-ttu-id="547d5-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="547d5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="547d5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="547d5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="547d5-105">Ein Array von ganzen Zahlen in einem angegebenen Intervall erhalten.</span><span class="sxs-lookup"><span data-stu-id="547d5-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="547d5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="547d5-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="547d5-107">von: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="547d5-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="547d5-108">Ein inklusiver Start Index des Intervalls.</span><span class="sxs-lookup"><span data-stu-id="547d5-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="547d5-109">an: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="547d5-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="547d5-110">Ein inklusiver Endindex des Intervalls, das nicht kleiner als ist `from` .</span><span class="sxs-lookup"><span data-stu-id="547d5-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="547d5-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="547d5-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="547d5-112">Ein Array, das die Reihenfolge der Zahlen `from` , `from + 1` ,..., enthält `to` .</span><span class="sxs-lookup"><span data-stu-id="547d5-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="remarks"></a><span data-ttu-id="547d5-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="547d5-113">Remarks</span></span>

<span data-ttu-id="547d5-114">Der Unterschied zwischen `from` und `to` muss in einen- `Int` Wert passen.</span><span class="sxs-lookup"><span data-stu-id="547d5-114">The difference between `from` and `to` must fit into an `Int` value.</span></span>