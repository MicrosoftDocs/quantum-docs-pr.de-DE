---
uid: Microsoft.Quantum.Canon.ApplyIfOne
title: Applyifone-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOne
qsharp.summary: Applies an operation conditioned on a classical result value being one.
ms.openlocfilehash: b86aecf3dc3d02d1a6bf0c112bdc45a55a2cf087
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841781"
---
# <a name="applyifone-operation"></a><span data-ttu-id="873fe-102">Applyifone-Vorgang</span><span class="sxs-lookup"><span data-stu-id="873fe-102">ApplyIfOne operation</span></span>

<span data-ttu-id="873fe-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="873fe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="873fe-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="873fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="873fe-105">Wendet einen Vorgang an, der von einem klassischen Ergebniswert abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="873fe-105">Applies an operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOne<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="873fe-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="873fe-106">Description</span></span>

<span data-ttu-id="873fe-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `One` .</span><span class="sxs-lookup"><span data-stu-id="873fe-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="873fe-108">Gibt `Zero` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="873fe-108">If `Zero`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="873fe-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="873fe-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="873fe-110">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="873fe-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="873fe-111">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="873fe-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="873fe-112">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="873fe-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="873fe-113">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="873fe-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="873fe-114">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="873fe-114">target : 'T</span></span>

<span data-ttu-id="873fe-115">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="873fe-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="873fe-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="873fe-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="873fe-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="873fe-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="873fe-118">GIF</span><span class="sxs-lookup"><span data-stu-id="873fe-118">'T</span></span>

<span data-ttu-id="873fe-119">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="873fe-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="873fe-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="873fe-120">See Also</span></span>

- [<span data-ttu-id="873fe-121">Microsoft. Quantum. Canon. applyifonec</span><span class="sxs-lookup"><span data-stu-id="873fe-121">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="873fe-122">Microsoft. Quantum. Canon. applyifonea</span><span class="sxs-lookup"><span data-stu-id="873fe-122">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="873fe-123">Microsoft. Quantum. Canon. applyifoneca</span><span class="sxs-lookup"><span data-stu-id="873fe-123">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)