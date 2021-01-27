---
uid: Microsoft.Quantum.Canon.RepeatA
title: Wiederholungs ATA-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 9ae3123a64b2a886df3b7575b2840522f9b011ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852221"
---
# <a name="repeata-operation"></a><span data-ttu-id="77b22-102">Wiederholungs ATA-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77b22-102">RepeatA operation</span></span>

<span data-ttu-id="77b22-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="77b22-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="77b22-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="77b22-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="77b22-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="77b22-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="77b22-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77b22-106">Input</span></span>

### <a name="op--tinput--unit--is-adj"></a><span data-ttu-id="77b22-107">OP: ' TInput => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="77b22-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="77b22-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="77b22-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="77b22-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="77b22-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="77b22-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="77b22-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="77b22-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="77b22-111">input : 'TInput</span></span>

<span data-ttu-id="77b22-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="77b22-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="77b22-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77b22-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="77b22-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="77b22-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="77b22-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="77b22-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="77b22-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="77b22-116">Example</span></span>

<span data-ttu-id="77b22-117">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="77b22-117">The following are equivalent:</span></span>

```qsharp
RepeatA(U, 17, target);
(BoundA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="77b22-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="77b22-118">See Also</span></span>

- [<span data-ttu-id="77b22-119">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="77b22-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="77b22-120">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="77b22-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="77b22-121">Microsoft. Quantum. Canon. repeatc</span><span class="sxs-lookup"><span data-stu-id="77b22-121">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="77b22-122">Microsoft. Quantum. Canon. repeatca</span><span class="sxs-lookup"><span data-stu-id="77b22-122">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)