---
uid: Microsoft.Quantum.Canon.RepeatC
title: Repeatc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: efb820411be63352fc09ada2441a9140dd5575f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840264"
---
# <a name="repeatc-operation"></a><span data-ttu-id="f4e12-102">Repeatc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f4e12-102">RepeatC operation</span></span>

<span data-ttu-id="f4e12-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f4e12-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f4e12-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f4e12-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f4e12-105">Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="f4e12-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="f4e12-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f4e12-106">Input</span></span>

### <a name="op--tinput--unit--is-ctl"></a><span data-ttu-id="f4e12-107">OP: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="f4e12-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="f4e12-108">Der Vorgang, der wiederholt aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4e12-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="f4e12-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4e12-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4e12-110">Die Anzahl der aufzurufenden Versuche `op` .</span><span class="sxs-lookup"><span data-stu-id="f4e12-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="f4e12-111">Eingabe: ' TInput</span><span class="sxs-lookup"><span data-stu-id="f4e12-111">input : 'TInput</span></span>

<span data-ttu-id="f4e12-112">Die an zu über gebenden Eingaben `op` .</span><span class="sxs-lookup"><span data-stu-id="f4e12-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f4e12-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f4e12-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f4e12-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f4e12-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="f4e12-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="f4e12-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="f4e12-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f4e12-116">Example</span></span>

<span data-ttu-id="f4e12-117">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="f4e12-117">The following are equivalent:</span></span>

```qsharp
RepeatC(U, 17, target);
(BoundC(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="f4e12-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f4e12-118">See Also</span></span>

- [<span data-ttu-id="f4e12-119">Microsoft. Quantum. Arrays. drawmany</span><span class="sxs-lookup"><span data-stu-id="f4e12-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="f4e12-120">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="f4e12-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="f4e12-121">Microsoft. Quantum. Canon. repeata</span><span class="sxs-lookup"><span data-stu-id="f4e12-121">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="f4e12-122">Microsoft. Quantum. Canon. repeatca</span><span class="sxs-lookup"><span data-stu-id="f4e12-122">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)