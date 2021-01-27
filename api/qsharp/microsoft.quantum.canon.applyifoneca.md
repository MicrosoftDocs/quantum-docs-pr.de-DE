---
uid: Microsoft.Quantum.Canon.ApplyIfOneCA
title: Applyifoneca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being one.
ms.openlocfilehash: 8b27a192c66a127fe5a8acfbba7b78314988bf2e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844911"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="8712e-102">Applyifoneca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8712e-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="8712e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8712e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8712e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8712e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8712e-105">Wendet einen einheitlichen Vorgang an, der auf einen klassischen Ergebniswert zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="8712e-105">Applies a unitary operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="8712e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8712e-106">Description</span></span>

<span data-ttu-id="8712e-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `One` .</span><span class="sxs-lookup"><span data-stu-id="8712e-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="8712e-108">Gibt `Zero` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="8712e-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="8712e-109">Das-Suffix `CA` gibt an, dass der anzuwendende Vorgang einheitlich (steuerbar und adjointable) ist.</span><span class="sxs-lookup"><span data-stu-id="8712e-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="8712e-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8712e-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="8712e-111">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="8712e-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="8712e-112">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8712e-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="8712e-113">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8712e-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8712e-114">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8712e-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="8712e-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="8712e-115">target : 'T</span></span>

<span data-ttu-id="8712e-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8712e-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8712e-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8712e-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8712e-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8712e-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8712e-119">GIF</span><span class="sxs-lookup"><span data-stu-id="8712e-119">'T</span></span>

<span data-ttu-id="8712e-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8712e-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="8712e-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8712e-121">See Also</span></span>

- [<span data-ttu-id="8712e-122">Microsoft. Quantum. Canon. applyifonec</span><span class="sxs-lookup"><span data-stu-id="8712e-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="8712e-123">Microsoft. Quantum. Canon. applyifonea</span><span class="sxs-lookup"><span data-stu-id="8712e-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="8712e-124">Microsoft. Quantum. Canon. applyifoneca</span><span class="sxs-lookup"><span data-stu-id="8712e-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)