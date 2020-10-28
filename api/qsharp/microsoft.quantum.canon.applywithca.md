---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: Applywithca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: abc62791416e78c1b2937a226327b71da8b8e288
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704578"
---
# <a name="applywithca-operation"></a><span data-ttu-id="43236-102">Applywithca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="43236-102">ApplyWithCA operation</span></span>

<span data-ttu-id="43236-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="43236-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="43236-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="43236-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="43236-105">Bei zwei Vorgängen wird eine als konjugated mit dem anderen angewendet.</span><span class="sxs-lookup"><span data-stu-id="43236-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="43236-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43236-106">Description</span></span>

<span data-ttu-id="43236-107">Bei zwei Vorgängen, die durch einheitliche Operatoren $U $ und $V $ beschrieben werden, wendet Sie diese in der Sequenz $U ^ {\dagger} V U $ an.</span><span class="sxs-lookup"><span data-stu-id="43236-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="43236-108">Das heißt, dieser Vorgang implementiert den einheitlichen Operator, der durch $V $-konjugated mit $U $ angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="43236-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="43236-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="43236-109">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="43236-110">outeroperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="43236-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="43236-111">Der Vorgang $U $, der für die konjugierte $V $ verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43236-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="43236-112">Beachten Sie, dass der äußere Vorgang $U $ adjointable sein muss, aber nicht steuerbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="43236-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit-adj--ctl"></a><span data-ttu-id="43236-113">inneroperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="43236-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="43236-114">Der Vorgang $V $ konjugated.</span><span class="sxs-lookup"><span data-stu-id="43236-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="43236-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="43236-115">target : 'T</span></span>

<span data-ttu-id="43236-116">Die Eingabe, die für den äußeren und inneren Vorgang bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="43236-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="43236-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43236-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="43236-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="43236-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="43236-119">GIF</span><span class="sxs-lookup"><span data-stu-id="43236-119">'T</span></span>

<span data-ttu-id="43236-120">Das Ziel, für das die einzelnen inneren und äußeren Operationen fungieren.</span><span class="sxs-lookup"><span data-stu-id="43236-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="43236-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="43236-121">Remarks</span></span>

<span data-ttu-id="43236-122">Der äußere Vorgang wird immer als adjointable angenommen, er muss jedoch nicht steuerbar sein, damit der kombinierte Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="43236-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="43236-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="43236-123">See Also</span></span>

- [<span data-ttu-id="43236-124">Microsoft. Quantum. Canon. applywith</span><span class="sxs-lookup"><span data-stu-id="43236-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="43236-125">Microsoft. Quantum. Canon. applyvon</span><span class="sxs-lookup"><span data-stu-id="43236-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="43236-126">Microsoft. Quantum. Canon. applywithc</span><span class="sxs-lookup"><span data-stu-id="43236-126">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)