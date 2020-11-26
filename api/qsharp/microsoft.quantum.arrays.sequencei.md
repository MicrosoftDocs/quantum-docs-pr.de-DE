---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Sequencei-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 5f03e5f2baff8077c1fa3fb5f1f079528ef0e215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220296"
---
# <a name="sequencei-function"></a><span data-ttu-id="4a476-102">Sequencei-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a476-102">SequenceI function</span></span>

<span data-ttu-id="4a476-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4a476-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4a476-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a476-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a476-105">Ein Array von ganzen Zahlen in einem angegebenen Intervall erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a476-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="4a476-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a476-106">Input</span></span>

### <a name="from--int"></a><span data-ttu-id="4a476-107">von: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a476-107">from : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4a476-108">Ein inklusiver Start Index des Intervalls.</span><span class="sxs-lookup"><span data-stu-id="4a476-108">An inclusive start index of the interval.</span></span>


### <a name="to--int"></a><span data-ttu-id="4a476-109">zu: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a476-109">to : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4a476-110">Ein inklusiver Endindex des Intervalls, das nicht kleiner als ist `from` .</span><span class="sxs-lookup"><span data-stu-id="4a476-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--int"></a><span data-ttu-id="4a476-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4a476-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4a476-112">Ein Array, das die Reihenfolge der Zahlen `from` , `from + 1` ,..., enthält `to` .</span><span class="sxs-lookup"><span data-stu-id="4a476-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>