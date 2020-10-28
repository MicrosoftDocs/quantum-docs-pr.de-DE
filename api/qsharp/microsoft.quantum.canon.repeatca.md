---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Repeatca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: b68c3aa4298fffa76f7c43ac4c6d27cdf3b72fbf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703859"
---
# <a name="repeatca-operation"></a><span data-ttu-id="5cdf4-102">Repeatca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5cdf4-102">RepeatCA operation</span></span>

<span data-ttu-id="5cdf4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5cdf4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5cdf4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5cdf4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5cdf4-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="5cdf4-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="5cdf4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5cdf4-106">Input</span></span>

### <a name="op--tinput--unit-adj--ctl"></a><span data-ttu-id="5cdf4-107">OP: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="5cdf4-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="5cdf4-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5cdf4-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="5cdf4-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5cdf4-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5cdf4-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="5cdf4-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="5cdf4-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="5cdf4-111">input : 'TInput</span></span>

<span data-ttu-id="5cdf4-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="5cdf4-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5cdf4-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5cdf4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5cdf4-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="5cdf4-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="5cdf4-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="5cdf4-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="5cdf4-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5cdf4-116">See Also</span></span>

- [<span data-ttu-id="5cdf4-117">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="5cdf4-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="5cdf4-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="5cdf4-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="5cdf4-119">Microsoft. Quantum. Canon. repeata</span><span class="sxs-lookup"><span data-stu-id="5cdf4-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="5cdf4-120">Microsoft. Quantum. Canon. repeatc</span><span class="sxs-lookup"><span data-stu-id="5cdf4-120">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)