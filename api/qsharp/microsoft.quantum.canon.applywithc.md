---
uid: Microsoft.Quantum.Canon.ApplyWithC
title: Applywithc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithC
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: 393db9f8ce092100abc157ace1ee9fbbb3b06d24
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850390"
---
# <a name="applywithc-operation"></a><span data-ttu-id="34219-102">Applywithc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="34219-102">ApplyWithC operation</span></span>

<span data-ttu-id="34219-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="34219-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="34219-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="34219-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="34219-105">Bei zwei Vorgängen wird eine als konjugated mit dem anderen angewendet.</span><span class="sxs-lookup"><span data-stu-id="34219-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithC<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Ctl), target : 'T) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="34219-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34219-106">Description</span></span>

<span data-ttu-id="34219-107">Bei zwei Vorgängen, die durch einheitliche Operatoren $U $ und $V $ beschrieben werden, wendet Sie diese in der Sequenz $U ^ {\dagger} V U $ an.</span><span class="sxs-lookup"><span data-stu-id="34219-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="34219-108">Das heißt, dieser Vorgang implementiert den einheitlichen Operator, der durch $V $-konjugated mit $U $ angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="34219-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="34219-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34219-109">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="34219-110">outeroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="34219-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="34219-111">Der Vorgang $U $, der für die konjugierte $V $ verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="34219-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="34219-112">Beachten Sie, dass der äußere Vorgang $U $ adjointable sein muss, aber nicht steuerbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="34219-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-ctl"></a><span data-ttu-id="34219-113">inneroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="34219-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="34219-114">Der Vorgang $V $ konjugated.</span><span class="sxs-lookup"><span data-stu-id="34219-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="34219-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="34219-115">target : 'T</span></span>

<span data-ttu-id="34219-116">Die Eingabe, die für den äußeren und inneren Vorgang bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="34219-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="34219-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="34219-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="34219-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="34219-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="34219-119">GIF</span><span class="sxs-lookup"><span data-stu-id="34219-119">'T</span></span>

<span data-ttu-id="34219-120">Das Ziel, für das die einzelnen inneren und äußeren Operationen fungieren.</span><span class="sxs-lookup"><span data-stu-id="34219-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="34219-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34219-121">Remarks</span></span>

<span data-ttu-id="34219-122">Der äußere Vorgang wird immer als adjointable angenommen, er muss jedoch nicht steuerbar sein, damit der kombinierte Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="34219-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="34219-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="34219-123">See Also</span></span>

- [<span data-ttu-id="34219-124">Microsoft. Quantum. Canon. applywith</span><span class="sxs-lookup"><span data-stu-id="34219-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="34219-125">Microsoft. Quantum. Canon. applyvon</span><span class="sxs-lookup"><span data-stu-id="34219-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="34219-126">Microsoft. Quantum. Canon. applywithca</span><span class="sxs-lookup"><span data-stu-id="34219-126">Microsoft.Quantum.Canon.ApplyWithCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithCA)