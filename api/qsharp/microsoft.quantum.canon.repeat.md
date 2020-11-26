---
uid: Microsoft.Quantum.Canon.Repeat
title: Wiederholungs Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: cd572e5e082df94d762a0869ad2c1923fb71fd3d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205591"
---
# <a name="repeat-operation"></a><span data-ttu-id="ad429-102">Wiederholungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="ad429-102">Repeat operation</span></span>

<span data-ttu-id="ad429-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ad429-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ad429-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ad429-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ad429-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="ad429-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="ad429-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad429-106">Input</span></span>

### <a name="op--tinput--unit"></a><span data-ttu-id="ad429-107">OP: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ad429-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ad429-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad429-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="ad429-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ad429-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ad429-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="ad429-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="ad429-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="ad429-111">input : 'TInput</span></span>

<span data-ttu-id="ad429-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="ad429-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ad429-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ad429-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ad429-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ad429-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="ad429-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="ad429-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="ad429-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad429-116">See Also</span></span>

- [<span data-ttu-id="ad429-117">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="ad429-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="ad429-118">Microsoft. Quantum. Canon. repeata</span><span class="sxs-lookup"><span data-stu-id="ad429-118">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="ad429-119">Microsoft. Quantum. Canon. repeatc</span><span class="sxs-lookup"><span data-stu-id="ad429-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="ad429-120">Microsoft. Quantum. Canon. repeatca</span><span class="sxs-lookup"><span data-stu-id="ad429-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)