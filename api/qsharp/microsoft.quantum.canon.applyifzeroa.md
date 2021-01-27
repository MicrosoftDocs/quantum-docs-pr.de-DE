---
uid: Microsoft.Quantum.Canon.ApplyIfZeroA
title: Applyif zeroa-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being zero.
ms.openlocfilehash: 23c494d144ef61d40c3ca7a5de452472ffa70335
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844902"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="6dd8e-102">Applyif zeroa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6dd8e-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="6dd8e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6dd8e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6dd8e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6dd8e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6dd8e-105">Wendet einen adjointable-Vorgang an, der von einem klassischen Ergebniswert von 0 (null) abhängt.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-105">Applies an adjointable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="6dd8e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6dd8e-106">Description</span></span>

<span data-ttu-id="6dd8e-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `Zero` .</span><span class="sxs-lookup"><span data-stu-id="6dd8e-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="6dd8e-108">Gibt `One` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="6dd8e-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="6dd8e-109">Das-Suffix `A` gibt an, dass der anzuwendende Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="6dd8e-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6dd8e-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="6dd8e-111">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6dd8e-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="6dd8e-112">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="6dd8e-113">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="6dd8e-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="6dd8e-114">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="6dd8e-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="6dd8e-115">target : 'T</span></span>

<span data-ttu-id="6dd8e-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6dd8e-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6dd8e-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6dd8e-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="6dd8e-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6dd8e-119">GIF</span><span class="sxs-lookup"><span data-stu-id="6dd8e-119">'T</span></span>

<span data-ttu-id="6dd8e-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="6dd8e-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6dd8e-121">See Also</span></span>

- [<span data-ttu-id="6dd8e-122">Microsoft. Quantum. Canon. applyif zeroc</span><span class="sxs-lookup"><span data-stu-id="6dd8e-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="6dd8e-123">Microsoft. Quantum. Canon. applyif zeroa</span><span class="sxs-lookup"><span data-stu-id="6dd8e-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="6dd8e-124">Microsoft. Quantum. Canon. applyif nuloca</span><span class="sxs-lookup"><span data-stu-id="6dd8e-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)