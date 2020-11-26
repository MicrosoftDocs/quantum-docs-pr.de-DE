---
uid: Microsoft.Quantum.Canon.RepeatC
title: Repeatc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 30fd172584b36601c4b81deff494cf55964518f2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205438"
---
# <a name="repeatc-operation"></a><span data-ttu-id="ec771-102">Repeatc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ec771-102">RepeatC operation</span></span>

<span data-ttu-id="ec771-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ec771-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ec771-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ec771-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ec771-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="ec771-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="ec771-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ec771-106">Input</span></span>

### <a name="op--tinput--unit--is-ctl"></a><span data-ttu-id="ec771-107">OP: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="ec771-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="ec771-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec771-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="ec771-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ec771-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ec771-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="ec771-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="ec771-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="ec771-111">input : 'TInput</span></span>

<span data-ttu-id="ec771-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="ec771-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ec771-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec771-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ec771-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ec771-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="ec771-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="ec771-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="ec771-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec771-116">See Also</span></span>

- [<span data-ttu-id="ec771-117">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="ec771-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="ec771-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="ec771-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="ec771-119">Microsoft. Quantum. Canon. repeata</span><span class="sxs-lookup"><span data-stu-id="ec771-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="ec771-120">Microsoft. Quantum. Canon. repeatca</span><span class="sxs-lookup"><span data-stu-id="ec771-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)