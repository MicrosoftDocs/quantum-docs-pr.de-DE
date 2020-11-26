---
uid: Microsoft.Quantum.Canon.ApplyIfOneC
title: Applyifonec-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being one.
ms.openlocfilehash: 24a00d83c1bbe6b07adb27c58fc70bc76af0a910
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209416"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="bc656-102">Applyifonec-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bc656-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="bc656-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bc656-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bc656-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bc656-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bc656-105">Wendet einen kontrollierbaren Vorgang an, der auf einen klassischen Ergebniswert zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="bc656-105">Applies a controllable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="bc656-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc656-106">Description</span></span>

<span data-ttu-id="bc656-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `One` .</span><span class="sxs-lookup"><span data-stu-id="bc656-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="bc656-108">Gibt `Zero` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="bc656-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="bc656-109">Das-Suffix `C` gibt an, dass der anzuwendende Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="bc656-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="bc656-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc656-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="bc656-111">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="bc656-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="bc656-112">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="bc656-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="bc656-113">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="bc656-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="bc656-114">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc656-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="bc656-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="bc656-115">target : 'T</span></span>

<span data-ttu-id="bc656-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="bc656-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bc656-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bc656-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bc656-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="bc656-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bc656-119">GIF</span><span class="sxs-lookup"><span data-stu-id="bc656-119">'T</span></span>

<span data-ttu-id="bc656-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc656-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc656-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bc656-121">See Also</span></span>

- [<span data-ttu-id="bc656-122">Microsoft. Quantum. Canon. applyifonec</span><span class="sxs-lookup"><span data-stu-id="bc656-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="bc656-123">Microsoft. Quantum. Canon. applyifonea</span><span class="sxs-lookup"><span data-stu-id="bc656-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="bc656-124">Microsoft. Quantum. Canon. applyifoneca</span><span class="sxs-lookup"><span data-stu-id="bc656-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)