---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Drawmany-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 3185f2ec01a2b9d01cff82a0c4667f12483801a7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209994"
---
# <a name="drawmany-operation"></a><span data-ttu-id="457c1-102">Drawmany-Vorgang</span><span class="sxs-lookup"><span data-stu-id="457c1-102">DrawMany operation</span></span>

<span data-ttu-id="457c1-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="457c1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="457c1-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="457c1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="457c1-105">Wiederholt einen Vorgang für eine bestimmte Anzahl von Samplings und sammelt die Ausgaben in einem Array.</span><span class="sxs-lookup"><span data-stu-id="457c1-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="457c1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="457c1-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="457c1-107">OP: ' TInput => ' TOutput</span><span class="sxs-lookup"><span data-stu-id="457c1-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="457c1-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="457c1-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="457c1-109">nsamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="457c1-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="457c1-110">Die Anzahl der Samplings zum Aufrufen von `op` zum Erfassen von.</span><span class="sxs-lookup"><span data-stu-id="457c1-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="457c1-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="457c1-111">input : 'TInput</span></span>

<span data-ttu-id="457c1-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="457c1-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="457c1-113">Ausgabe: ' TOutput []</span><span class="sxs-lookup"><span data-stu-id="457c1-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="457c1-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="457c1-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="457c1-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="457c1-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="457c1-116">"TOutput"</span><span class="sxs-lookup"><span data-stu-id="457c1-116">'TOutput</span></span>



## <a name="see-also"></a><span data-ttu-id="457c1-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="457c1-117">See Also</span></span>

- [<span data-ttu-id="457c1-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="457c1-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)