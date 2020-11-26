---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: Applywithca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: e86c452e9693c5a4d0d4e5a36471ab46bbf66dfe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208141"
---
# <a name="applywithca-operation"></a><span data-ttu-id="cb464-102">Applywithca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cb464-102">ApplyWithCA operation</span></span>

<span data-ttu-id="cb464-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cb464-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cb464-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cb464-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cb464-105">Bei zwei Vorgängen wird eine als konjugated mit dem anderen angewendet.</span><span class="sxs-lookup"><span data-stu-id="cb464-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="cb464-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb464-106">Description</span></span>

<span data-ttu-id="cb464-107">Bei zwei Vorgängen, die durch einheitliche Operatoren $U $ und $V $ beschrieben werden, wendet Sie diese in der Sequenz $U ^ {\dagger} V U $ an.</span><span class="sxs-lookup"><span data-stu-id="cb464-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="cb464-108">Das heißt, dieser Vorgang implementiert den einheitlichen Operator, der durch $V $-konjugated mit $U $ angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb464-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="cb464-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb464-109">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="cb464-110">outeroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="cb464-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="cb464-111">Der Vorgang $U $, der für die konjugierte $V $ verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb464-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="cb464-112">Beachten Sie, dass der äußere Vorgang $U $ adjointable sein muss, aber nicht steuerbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="cb464-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj--ctl"></a><span data-ttu-id="cb464-113">inneroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="cb464-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="cb464-114">Der Vorgang $V $ konjugated.</span><span class="sxs-lookup"><span data-stu-id="cb464-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="cb464-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="cb464-115">target : 'T</span></span>

<span data-ttu-id="cb464-116">Die Eingabe, die für den äußeren und inneren Vorgang bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb464-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cb464-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cb464-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cb464-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="cb464-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cb464-119">GIF</span><span class="sxs-lookup"><span data-stu-id="cb464-119">'T</span></span>

<span data-ttu-id="cb464-120">Das Ziel, für das die einzelnen inneren und äußeren Operationen fungieren.</span><span class="sxs-lookup"><span data-stu-id="cb464-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb464-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb464-121">Remarks</span></span>

<span data-ttu-id="cb464-122">Der äußere Vorgang wird immer als adjointable angenommen, er muss jedoch nicht steuerbar sein, damit der kombinierte Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="cb464-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb464-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cb464-123">See Also</span></span>

- [<span data-ttu-id="cb464-124">Microsoft. Quantum. Canon. applywith</span><span class="sxs-lookup"><span data-stu-id="cb464-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="cb464-125">Microsoft. Quantum. Canon. applyvon</span><span class="sxs-lookup"><span data-stu-id="cb464-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="cb464-126">Microsoft. Quantum. Canon. applywithc</span><span class="sxs-lookup"><span data-stu-id="cb464-126">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)