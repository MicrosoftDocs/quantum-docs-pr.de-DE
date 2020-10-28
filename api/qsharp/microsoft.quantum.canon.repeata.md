---
uid: Microsoft.Quantum.Canon.RepeatA
title: Wiederholungs ATA-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 89d34e5a30a61dee392904ce1076605432e21395
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703865"
---
# <a name="repeata-operation"></a><span data-ttu-id="9db17-102">Wiederholungs ATA-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9db17-102">RepeatA operation</span></span>

<span data-ttu-id="9db17-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9db17-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9db17-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9db17-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9db17-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="9db17-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="9db17-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9db17-106">Input</span></span>

### <a name="op--tinput--unit-adj"></a><span data-ttu-id="9db17-107">OP: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="9db17-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="9db17-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9db17-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="9db17-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9db17-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9db17-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="9db17-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="9db17-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="9db17-111">input : 'TInput</span></span>

<span data-ttu-id="9db17-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="9db17-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9db17-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9db17-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9db17-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9db17-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="9db17-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="9db17-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="9db17-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9db17-116">See Also</span></span>

- [<span data-ttu-id="9db17-117">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="9db17-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="9db17-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="9db17-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="9db17-119">Microsoft. Quantum. Canon. repeatc</span><span class="sxs-lookup"><span data-stu-id="9db17-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="9db17-120">Microsoft. Quantum. Canon. repeatca</span><span class="sxs-lookup"><span data-stu-id="9db17-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)