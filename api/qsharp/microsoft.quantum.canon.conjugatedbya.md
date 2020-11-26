---
uid: Microsoft.Quantum.Canon.ConjugatedByA
title: Konkanable-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByA
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: eaa104039b857f0469ddc0aaba97698eca20860d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207342"
---
# <a name="conjugatedbya-function"></a><span data-ttu-id="c43ab-102">Konkanable-Funktion</span><span class="sxs-lookup"><span data-stu-id="c43ab-102">ConjugatedByA function</span></span>

<span data-ttu-id="c43ab-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c43ab-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c43ab-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c43ab-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c43ab-105">Bei den äußeren und inneren Vorgängen wird ein neuer Vorgang zurückgegeben, der den inneren Vorgang durch den äußeren Vorgang konjugiert.</span><span class="sxs-lookup"><span data-stu-id="c43ab-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedByA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj)) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="c43ab-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c43ab-106">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="c43ab-107">outeroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="c43ab-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c43ab-108">Der Vorgang $U $, der für die konjugierte $V $ verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c43ab-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="c43ab-109">Beachten Sie, dass der äußere Vorgang $U $ adjointable sein muss, aber nicht steuerbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="c43ab-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj"></a><span data-ttu-id="c43ab-110">inneroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="c43ab-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c43ab-111">Der Vorgang $V $ konjugated.</span><span class="sxs-lookup"><span data-stu-id="c43ab-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="c43ab-112">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="c43ab-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c43ab-113">Ein neuer Vorgang, dessen Aktion durch die einheitliche $U ^ {\dagger} V U $ dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c43ab-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c43ab-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c43ab-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c43ab-115">GIF</span><span class="sxs-lookup"><span data-stu-id="c43ab-115">'T</span></span>

<span data-ttu-id="c43ab-116">Der Typ des Ziels, für das die einzelnen inneren und äußeren Operationen agieren.</span><span class="sxs-lookup"><span data-stu-id="c43ab-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="c43ab-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c43ab-117">Remarks</span></span>

<span data-ttu-id="c43ab-118">Der äußere Vorgang wird immer als adjointable angenommen, er muss jedoch nicht steuerbar sein, damit der kombinierte Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="c43ab-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="c43ab-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c43ab-119">See Also</span></span>

- [<span data-ttu-id="c43ab-120">Microsoft. Quantum. Canon. Kon.</span><span class="sxs-lookup"><span data-stu-id="c43ab-120">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="c43ab-121">Microsoft. Quantum.......</span><span class="sxs-lookup"><span data-stu-id="c43ab-121">Microsoft.Quantum.Canon.ConjugatedByC</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [<span data-ttu-id="c43ab-122">Microsoft. Quantum. Canon. konkanonische byca</span><span class="sxs-lookup"><span data-stu-id="c43ab-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="c43ab-123">Microsoft. Quantum. Canon. applywith</span><span class="sxs-lookup"><span data-stu-id="c43ab-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)