---
uid: Microsoft.Quantum.Canon.Repeat
title: Wiederholungs Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5aedd056b851b8d8d7c25a32eb22587292e132a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703878"
---
# <a name="repeat-operation"></a><span data-ttu-id="d0f61-102">Wiederholungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="d0f61-102">Repeat operation</span></span>

<span data-ttu-id="d0f61-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d0f61-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d0f61-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0f61-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0f61-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="d0f61-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="d0f61-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d0f61-106">Input</span></span>

### <a name="op--tinput--unit"></a><span data-ttu-id="d0f61-107">OP: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0f61-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d0f61-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0f61-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="d0f61-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d0f61-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d0f61-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="d0f61-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="d0f61-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="d0f61-111">input : 'TInput</span></span>

<span data-ttu-id="d0f61-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="d0f61-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d0f61-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0f61-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d0f61-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d0f61-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="d0f61-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="d0f61-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="d0f61-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0f61-116">See Also</span></span>

- [<span data-ttu-id="d0f61-117">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="d0f61-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="d0f61-118">Microsoft. Quantum. Canon. repeata</span><span class="sxs-lookup"><span data-stu-id="d0f61-118">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="d0f61-119">Microsoft. Quantum. Canon. repeatc</span><span class="sxs-lookup"><span data-stu-id="d0f61-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="d0f61-120">Microsoft. Quantum. Canon. repeatca</span><span class="sxs-lookup"><span data-stu-id="d0f61-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)