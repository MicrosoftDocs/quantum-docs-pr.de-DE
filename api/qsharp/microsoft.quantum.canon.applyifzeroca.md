---
uid: Microsoft.Quantum.Canon.ApplyIfZeroCA
title: Applyif nuloca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being zero.
ms.openlocfilehash: 4baae1fe7d615cbbf01935b4eca05fe947ff296e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218460"
---
# <a name="applyifzeroca-operation"></a><span data-ttu-id="782f1-102">Applyif nuloca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="782f1-102">ApplyIfZeroCA operation</span></span>

<span data-ttu-id="782f1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="782f1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="782f1-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="782f1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="782f1-105">Wendet einen einheitlichen Vorgang an, der auf einem klassischen Ergebniswert von 0 (null) liegt.</span><span class="sxs-lookup"><span data-stu-id="782f1-105">Applies a unitary operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="782f1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="782f1-106">Description</span></span>

<span data-ttu-id="782f1-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `Zero` .</span><span class="sxs-lookup"><span data-stu-id="782f1-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="782f1-108">Gibt `One` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="782f1-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="782f1-109">Das-Suffix `CA` gibt an, dass der anzuwendende Vorgang einheitlich (steuerbar und adjointable) ist.</span><span class="sxs-lookup"><span data-stu-id="782f1-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="782f1-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="782f1-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="782f1-111">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="782f1-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="782f1-112">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="782f1-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="782f1-113">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="782f1-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="782f1-114">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="782f1-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="782f1-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="782f1-115">target : 'T</span></span>

<span data-ttu-id="782f1-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="782f1-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="782f1-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="782f1-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="782f1-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="782f1-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="782f1-119">GIF</span><span class="sxs-lookup"><span data-stu-id="782f1-119">'T</span></span>

<span data-ttu-id="782f1-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="782f1-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="782f1-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="782f1-121">See Also</span></span>

- [<span data-ttu-id="782f1-122">Microsoft. Quantum. Canon. applyif zeroc</span><span class="sxs-lookup"><span data-stu-id="782f1-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="782f1-123">Microsoft. Quantum. Canon. applyif zeroa</span><span class="sxs-lookup"><span data-stu-id="782f1-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="782f1-124">Microsoft. Quantum. Canon. applyif nuloca</span><span class="sxs-lookup"><span data-stu-id="782f1-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)