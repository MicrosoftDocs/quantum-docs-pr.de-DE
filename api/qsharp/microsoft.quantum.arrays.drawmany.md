---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Drawmany-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: bf63ce308679cef97c776d3383ff732ed4d4e500
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846202"
---
# <a name="drawmany-operation"></a><span data-ttu-id="7331c-102">Drawmany-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7331c-102">DrawMany operation</span></span>

<span data-ttu-id="7331c-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7331c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7331c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7331c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7331c-105">Wiederholt einen Vorgang für eine bestimmte Anzahl von Samplings und sammelt die Ausgaben in einem Array.</span><span class="sxs-lookup"><span data-stu-id="7331c-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="7331c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7331c-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="7331c-107">OP: ' TInput => ' TOutput</span><span class="sxs-lookup"><span data-stu-id="7331c-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="7331c-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7331c-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="7331c-109">nsamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7331c-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7331c-110">Die Anzahl der Samplings zum Aufrufen von `op` zum Erfassen von.</span><span class="sxs-lookup"><span data-stu-id="7331c-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="7331c-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="7331c-111">input : 'TInput</span></span>

<span data-ttu-id="7331c-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="7331c-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="7331c-113">Ausgabe: ' TOutput []</span><span class="sxs-lookup"><span data-stu-id="7331c-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7331c-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7331c-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="7331c-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="7331c-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="7331c-116">"TOutput"</span><span class="sxs-lookup"><span data-stu-id="7331c-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="7331c-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7331c-117">Example</span></span>

<span data-ttu-id="7331c-118">Im folgenden Beispiel wird eine ganze Zahl bei einem Vorgang, der ein einzelnes Bit Abtastungen, als Stichprobe betrachtet.</span><span class="sxs-lookup"><span data-stu-id="7331c-118">The following samples an integer, given an operation that samples a single bit at a time.</span></span>

```qsharp
let randomInteger = BoolArrayAsInt(DrawMany(SampleRandomBit, 16, ()));
```

## <a name="see-also"></a><span data-ttu-id="7331c-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7331c-119">See Also</span></span>

- [<span data-ttu-id="7331c-120">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="7331c-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)