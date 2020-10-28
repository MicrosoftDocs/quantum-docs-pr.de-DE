---
uid: Microsoft.Quantum.Canon.ConjugatedByC
title: Konkanable-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByC
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: c4c381e40c5a941487bcf78ebe5339574aedb45d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704335"
---
# <a name="conjugatedbyc-function"></a><span data-ttu-id="50036-102">Konkanable-Funktion</span><span class="sxs-lookup"><span data-stu-id="50036-102">ConjugatedByC function</span></span>

<span data-ttu-id="50036-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="50036-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="50036-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="50036-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="50036-105">Bei den äußeren und inneren Vorgängen wird ein neuer Vorgang zurückgegeben, der den inneren Vorgang durch den äußeren Vorgang konjugiert.</span><span class="sxs-lookup"><span data-stu-id="50036-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedByC<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Ctl)) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="50036-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50036-106">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="50036-107">outeroperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="50036-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="50036-108">Der Vorgang $U $, der für die konjugierte $V $ verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="50036-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="50036-109">Beachten Sie, dass der äußere Vorgang $U $ adjointable sein muss, aber nicht steuerbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="50036-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit-ctl"></a><span data-ttu-id="50036-110">inneroperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="50036-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="50036-111">Der Vorgang $V $ konjugated.</span><span class="sxs-lookup"><span data-stu-id="50036-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit-ctl"></a><span data-ttu-id="50036-112">Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="50036-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="50036-113">Ein neuer Vorgang, dessen Aktion durch die einheitliche $U ^ {\dagger} V U $ dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="50036-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="50036-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="50036-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="50036-115">GIF</span><span class="sxs-lookup"><span data-stu-id="50036-115">'T</span></span>

<span data-ttu-id="50036-116">Der Typ des Ziels, für das die einzelnen inneren und äußeren Operationen agieren.</span><span class="sxs-lookup"><span data-stu-id="50036-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="50036-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50036-117">Remarks</span></span>

<span data-ttu-id="50036-118">Der äußere Vorgang wird immer als adjointable angenommen, er muss jedoch nicht steuerbar sein, damit der kombinierte Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="50036-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="50036-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50036-119">See Also</span></span>

- [<span data-ttu-id="50036-120">Microsoft. Quantum. Canon. konkanoniedby</span><span class="sxs-lookup"><span data-stu-id="50036-120">Microsoft.Quantum.Canon.ConjugatedBy</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedBy)
- [<span data-ttu-id="50036-121">Microsoft. Quantum. Canon. Kon.</span><span class="sxs-lookup"><span data-stu-id="50036-121">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="50036-122">Microsoft. Quantum. Canon. konkanonische byca</span><span class="sxs-lookup"><span data-stu-id="50036-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="50036-123">Microsoft. Quantum. Canon. applywith</span><span class="sxs-lookup"><span data-stu-id="50036-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)