---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Repeatca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: af93220562d6be27b2f41e770bd953e5e808fcbf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852208"
---
# <a name="repeatca-operation"></a><span data-ttu-id="b018d-102">Repeatca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b018d-102">RepeatCA operation</span></span>

<span data-ttu-id="b018d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b018d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b018d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b018d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b018d-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="b018d-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b018d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b018d-106">Input</span></span>

### <a name="op--tinput--unit--is-adj--ctl"></a><span data-ttu-id="b018d-107">OP: ' TInput => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="b018d-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="b018d-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b018d-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="b018d-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b018d-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b018d-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="b018d-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="b018d-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="b018d-111">input : 'TInput</span></span>

<span data-ttu-id="b018d-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="b018d-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b018d-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b018d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b018d-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b018d-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="b018d-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="b018d-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="b018d-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b018d-116">Example</span></span>

<span data-ttu-id="b018d-117">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="b018d-117">The following are equivalent:</span></span>

```qsharp
RepeatCA(U, 17, target);
(BoundCA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="b018d-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b018d-118">See Also</span></span>

- [<span data-ttu-id="b018d-119">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="b018d-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="b018d-120">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="b018d-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="b018d-121">Microsoft. Quantum. Canon. repeata</span><span class="sxs-lookup"><span data-stu-id="b018d-121">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="b018d-122">Microsoft. Quantum. Canon. repeatc</span><span class="sxs-lookup"><span data-stu-id="b018d-122">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)