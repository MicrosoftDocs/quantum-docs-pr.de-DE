---
uid: Microsoft.Quantum.Canon.ApplyIfOneCA
title: Applyifoneca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being one.
ms.openlocfilehash: 973dd3c5f9f3e9ad03c0626a38779f499b7ce657
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705255"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="c7b83-102">Applyifoneca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c7b83-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="c7b83-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c7b83-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c7b83-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c7b83-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c7b83-105">Wendet einen einheitlichen Vorgang an, der auf einen klassischen Ergebniswert zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="c7b83-105">Applies a unitary operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="c7b83-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7b83-106">Description</span></span>

<span data-ttu-id="c7b83-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `One` .</span><span class="sxs-lookup"><span data-stu-id="c7b83-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="c7b83-108">Gibt `Zero` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="c7b83-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="c7b83-109">Das-Suffix `CA` gibt an, dass der anzuwendende Vorgang einheitlich (steuerbar und adjointable) ist.</span><span class="sxs-lookup"><span data-stu-id="c7b83-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="c7b83-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7b83-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="c7b83-111">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="c7b83-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="c7b83-112">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7b83-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="c7b83-113">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="c7b83-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="c7b83-114">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7b83-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="c7b83-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="c7b83-115">target : 'T</span></span>

<span data-ttu-id="c7b83-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7b83-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c7b83-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7b83-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c7b83-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c7b83-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c7b83-119">GIF</span><span class="sxs-lookup"><span data-stu-id="c7b83-119">'T</span></span>

<span data-ttu-id="c7b83-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7b83-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7b83-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7b83-121">See Also</span></span>

- [<span data-ttu-id="c7b83-122">Microsoft. Quantum. Canon. applyifonec</span><span class="sxs-lookup"><span data-stu-id="c7b83-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="c7b83-123">Microsoft. Quantum. Canon. applyifonea</span><span class="sxs-lookup"><span data-stu-id="c7b83-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="c7b83-124">Microsoft. Quantum. Canon. applyifoneca</span><span class="sxs-lookup"><span data-stu-id="c7b83-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)