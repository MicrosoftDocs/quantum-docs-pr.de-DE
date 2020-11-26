---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: Applyifonea-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 200908f2958b74e4823c891ef901474d75d18336
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218545"
---
# <a name="applyifonea-operation"></a><span data-ttu-id="e8171-102">Applyifonea-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e8171-102">ApplyIfOneA operation</span></span>

<span data-ttu-id="e8171-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8171-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8171-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8171-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8171-105">Wendet einen adjointable-Vorgang an, der auf einen klassischen Ergebniswert zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="e8171-105">Applies an adjointable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="e8171-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8171-106">Description</span></span>

<span data-ttu-id="e8171-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `One` .</span><span class="sxs-lookup"><span data-stu-id="e8171-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="e8171-108">Gibt `Zero` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="e8171-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="e8171-109">Das-Suffix `A` gibt an, dass der anzuwendende Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="e8171-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="e8171-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8171-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="e8171-111">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="e8171-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="e8171-112">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8171-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="e8171-113">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="e8171-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e8171-114">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8171-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="e8171-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="e8171-115">target : 'T</span></span>

<span data-ttu-id="e8171-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8171-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8171-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8171-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e8171-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e8171-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e8171-119">GIF</span><span class="sxs-lookup"><span data-stu-id="e8171-119">'T</span></span>

<span data-ttu-id="e8171-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8171-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8171-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8171-121">See Also</span></span>

- [<span data-ttu-id="e8171-122">Microsoft. Quantum. Canon. applyifonec</span><span class="sxs-lookup"><span data-stu-id="e8171-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="e8171-123">Microsoft. Quantum. Canon. applyifonea</span><span class="sxs-lookup"><span data-stu-id="e8171-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="e8171-124">Microsoft. Quantum. Canon. applyifoneca</span><span class="sxs-lookup"><span data-stu-id="e8171-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)