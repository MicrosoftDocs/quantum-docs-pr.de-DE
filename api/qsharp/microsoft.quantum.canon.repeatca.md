---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Repeatca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 24606486b3d5703065a7c7f62d3bbc7e3d07615f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205404"
---
# <a name="repeatca-operation"></a><span data-ttu-id="f8afb-102">Repeatca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f8afb-102">RepeatCA operation</span></span>

<span data-ttu-id="f8afb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f8afb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f8afb-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f8afb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f8afb-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="f8afb-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f8afb-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f8afb-106">Input</span></span>

### <a name="op--tinput--unit--is-adj--ctl"></a><span data-ttu-id="f8afb-107">OP: ' TInput => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="f8afb-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f8afb-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8afb-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="f8afb-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f8afb-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f8afb-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="f8afb-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="f8afb-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="f8afb-111">input : 'TInput</span></span>

<span data-ttu-id="f8afb-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="f8afb-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f8afb-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f8afb-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f8afb-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f8afb-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="f8afb-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="f8afb-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="f8afb-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8afb-116">See Also</span></span>

- [<span data-ttu-id="f8afb-117">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="f8afb-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="f8afb-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="f8afb-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="f8afb-119">Microsoft. Quantum. Canon. repeata</span><span class="sxs-lookup"><span data-stu-id="f8afb-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="f8afb-120">Microsoft. Quantum. Canon. repeatc</span><span class="sxs-lookup"><span data-stu-id="f8afb-120">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)