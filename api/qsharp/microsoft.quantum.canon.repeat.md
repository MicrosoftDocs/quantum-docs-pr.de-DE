---
uid: Microsoft.Quantum.Canon.Repeat
title: Wiederholungs Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 40ee191e8d9044f33aa1621303c70f7e0847e8f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852243"
---
# <a name="repeat-operation"></a><span data-ttu-id="7d8cf-102">Wiederholungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="7d8cf-102">Repeat operation</span></span>

<span data-ttu-id="7d8cf-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7d8cf-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7d8cf-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7d8cf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7d8cf-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7d8cf-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="7d8cf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7d8cf-106">Input</span></span>

### <a name="op--tinput--unit"></a><span data-ttu-id="7d8cf-107">OP: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d8cf-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="7d8cf-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d8cf-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="7d8cf-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7d8cf-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7d8cf-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="7d8cf-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="7d8cf-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="7d8cf-111">input : 'TInput</span></span>

<span data-ttu-id="7d8cf-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="7d8cf-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7d8cf-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d8cf-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7d8cf-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7d8cf-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="7d8cf-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="7d8cf-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="7d8cf-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7d8cf-116">Example</span></span>

<span data-ttu-id="7d8cf-117">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="7d8cf-117">The following are equivalent:</span></span>

```qsharp
Repeat(U, 17, target);
(Bound(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="7d8cf-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7d8cf-118">See Also</span></span>

- [<span data-ttu-id="7d8cf-119">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="7d8cf-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="7d8cf-120">Microsoft. Quantum. Canon. repeata</span><span class="sxs-lookup"><span data-stu-id="7d8cf-120">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="7d8cf-121">Microsoft. Quantum. Canon. repeatc</span><span class="sxs-lookup"><span data-stu-id="7d8cf-121">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="7d8cf-122">Microsoft. Quantum. Canon. repeatca</span><span class="sxs-lookup"><span data-stu-id="7d8cf-122">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)