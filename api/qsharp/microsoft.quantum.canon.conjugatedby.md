---
uid: Microsoft.Quantum.Canon.ConjugatedBy
title: Kon-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedBy
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: c11e6b2cc97e682bf4fe266997f60ce69e87ba96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840879"
---
# <a name="conjugatedby-function"></a><span data-ttu-id="ec9b3-102">Kon-Funktion</span><span class="sxs-lookup"><span data-stu-id="ec9b3-102">ConjugatedBy function</span></span>

<span data-ttu-id="ec9b3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ec9b3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ec9b3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ec9b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ec9b3-105">Bei den äußeren und inneren Vorgängen wird ein neuer Vorgang zurückgegeben, der den inneren Vorgang durch den äußeren Vorgang konjugiert.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedBy<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit)) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="ec9b3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ec9b3-106">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="ec9b3-107">outeroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="ec9b3-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ec9b3-108">Der Vorgang $U $, der für die konjugierte $V $ verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="ec9b3-109">Beachten Sie, dass der äußere Vorgang $U $ adjointable sein muss, aber nicht steuerbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit"></a><span data-ttu-id="ec9b3-110">inneroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec9b3-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ec9b3-111">Der Vorgang $V $ konjugated.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="ec9b3-112">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec9b3-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ec9b3-113">Ein neuer Vorgang, dessen Aktion durch die einheitliche $U ^ {\dagger} V U $ dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ec9b3-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ec9b3-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ec9b3-115">GIF</span><span class="sxs-lookup"><span data-stu-id="ec9b3-115">'T</span></span>

<span data-ttu-id="ec9b3-116">Der Typ des Ziels, für das die einzelnen inneren und äußeren Operationen agieren.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec9b3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec9b3-117">Remarks</span></span>

<span data-ttu-id="ec9b3-118">Der äußere Vorgang wird immer als adjointable angenommen, er muss jedoch nicht steuerbar sein, damit der kombinierte Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec9b3-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec9b3-119">See Also</span></span>

- [<span data-ttu-id="ec9b3-120">Microsoft. Quantum. Canon. Kon.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-120">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="ec9b3-121">Microsoft. Quantum.......</span><span class="sxs-lookup"><span data-stu-id="ec9b3-121">Microsoft.Quantum.Canon.ConjugatedByC</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [<span data-ttu-id="ec9b3-122">Microsoft. Quantum. Canon. konkanonische byca</span><span class="sxs-lookup"><span data-stu-id="ec9b3-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="ec9b3-123">Microsoft. Quantum. Canon. applywith</span><span class="sxs-lookup"><span data-stu-id="ec9b3-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)