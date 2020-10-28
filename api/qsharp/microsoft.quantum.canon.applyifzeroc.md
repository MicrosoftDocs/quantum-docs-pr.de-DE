---
uid: Microsoft.Quantum.Canon.ApplyIfZeroC
title: Applyif zeroc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being zero.
ms.openlocfilehash: cfc2a659f4da011baadff1a0d6a20a2a36d0a285
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705223"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="12fb8-102">Applyif zeroc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="12fb8-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="12fb8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="12fb8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="12fb8-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12fb8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12fb8-105">Wendet einen für einen klassischen Ergebniswert bedingten Vorgang an, der 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="12fb8-105">Applies a controllable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="12fb8-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12fb8-106">Description</span></span>

<span data-ttu-id="12fb8-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `Zero` .</span><span class="sxs-lookup"><span data-stu-id="12fb8-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="12fb8-108">Gibt `One` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="12fb8-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="12fb8-109">Das-Suffix `C` gibt an, dass der anzuwendende Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="12fb8-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="12fb8-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="12fb8-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="12fb8-111">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="12fb8-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="12fb8-112">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="12fb8-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-ctl"></a><span data-ttu-id="12fb8-113">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="12fb8-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="12fb8-114">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="12fb8-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="12fb8-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="12fb8-115">target : 'T</span></span>

<span data-ttu-id="12fb8-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="12fb8-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="12fb8-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12fb8-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="12fb8-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="12fb8-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="12fb8-119">GIF</span><span class="sxs-lookup"><span data-stu-id="12fb8-119">'T</span></span>

<span data-ttu-id="12fb8-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="12fb8-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="12fb8-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="12fb8-121">See Also</span></span>

- [<span data-ttu-id="12fb8-122">Microsoft. Quantum. Canon. applyif zeroc</span><span class="sxs-lookup"><span data-stu-id="12fb8-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="12fb8-123">Microsoft. Quantum. Canon. applyif zeroa</span><span class="sxs-lookup"><span data-stu-id="12fb8-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="12fb8-124">Microsoft. Quantum. Canon. applyif nuloca</span><span class="sxs-lookup"><span data-stu-id="12fb8-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)