---
uid: Microsoft.Quantum.Canon.RepeatA
title: Wiederholungs ATA-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5f418f67d7265d4cb39b3636906c74d33d80f472
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205557"
---
# <a name="repeata-operation"></a><span data-ttu-id="2040f-102">Wiederholungs ATA-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2040f-102">RepeatA operation</span></span>

<span data-ttu-id="2040f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2040f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2040f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2040f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2040f-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="2040f-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="2040f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2040f-106">Input</span></span>

### <a name="op--tinput--unit--is-adj"></a><span data-ttu-id="2040f-107">OP: ' TInput => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="2040f-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="2040f-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2040f-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="2040f-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2040f-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2040f-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="2040f-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="2040f-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="2040f-111">input : 'TInput</span></span>

<span data-ttu-id="2040f-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="2040f-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2040f-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2040f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2040f-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2040f-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="2040f-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="2040f-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="2040f-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2040f-116">See Also</span></span>

- [<span data-ttu-id="2040f-117">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="2040f-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="2040f-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="2040f-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="2040f-119">Microsoft. Quantum. Canon. repeatc</span><span class="sxs-lookup"><span data-stu-id="2040f-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="2040f-120">Microsoft. Quantum. Canon. repeatca</span><span class="sxs-lookup"><span data-stu-id="2040f-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)