---
uid: Microsoft.Quantum.Canon.ApplyIfOne
title: Applyifone-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOne
qsharp.summary: Applies an operation conditioned on a classical result value being one.
ms.openlocfilehash: 8c668423d126f02736bcb541e73e210a761c5719
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705274"
---
# <a name="applyifone-operation"></a><span data-ttu-id="52a12-102">Applyifone-Vorgang</span><span class="sxs-lookup"><span data-stu-id="52a12-102">ApplyIfOne operation</span></span>

<span data-ttu-id="52a12-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="52a12-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="52a12-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="52a12-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="52a12-105">Wendet einen Vorgang an, der von einem klassischen Ergebniswert abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="52a12-105">Applies an operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOne<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="52a12-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52a12-106">Description</span></span>

<span data-ttu-id="52a12-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `One` .</span><span class="sxs-lookup"><span data-stu-id="52a12-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="52a12-108">Gibt `Zero` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="52a12-108">If `Zero`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="52a12-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="52a12-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="52a12-110">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="52a12-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="52a12-111">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="52a12-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="52a12-112">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52a12-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="52a12-113">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52a12-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="52a12-114">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="52a12-114">target : 'T</span></span>

<span data-ttu-id="52a12-115">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="52a12-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="52a12-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52a12-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="52a12-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="52a12-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="52a12-118">GIF</span><span class="sxs-lookup"><span data-stu-id="52a12-118">'T</span></span>

<span data-ttu-id="52a12-119">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52a12-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="52a12-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="52a12-120">See Also</span></span>

- [<span data-ttu-id="52a12-121">Microsoft. Quantum. Canon. applyifonec</span><span class="sxs-lookup"><span data-stu-id="52a12-121">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="52a12-122">Microsoft. Quantum. Canon. applyifonea</span><span class="sxs-lookup"><span data-stu-id="52a12-122">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="52a12-123">Microsoft. Quantum. Canon. applyifoneca</span><span class="sxs-lookup"><span data-stu-id="52a12-123">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)