---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Sequencei-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5dc4377c696e14b505c63701c2f5ca0dadca672
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705794"
---
# <a name="sequencei-function"></a><span data-ttu-id="15916-102">Sequencei-Funktion</span><span class="sxs-lookup"><span data-stu-id="15916-102">SequenceI function</span></span>

<span data-ttu-id="15916-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="15916-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="15916-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="15916-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="15916-105">Ein Array von ganzen Zahlen in einem angegebenen Intervall erhalten.</span><span class="sxs-lookup"><span data-stu-id="15916-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="15916-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="15916-106">Input</span></span>

### <a name="from--int"></a><span data-ttu-id="15916-107">von: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="15916-107">from : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="15916-108">Ein inklusiver Start Index des Intervalls.</span><span class="sxs-lookup"><span data-stu-id="15916-108">An inclusive start index of the interval.</span></span>


### <a name="to--int"></a><span data-ttu-id="15916-109">zu: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="15916-109">to : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="15916-110">Ein inklusiver Endindex des Intervalls, das nicht kleiner als ist `from` .</span><span class="sxs-lookup"><span data-stu-id="15916-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--int"></a><span data-ttu-id="15916-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="15916-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="15916-112">Ein Array, das die Reihenfolge der Zahlen `from` , `from + 1` ,..., enthält `to` .</span><span class="sxs-lookup"><span data-stu-id="15916-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>