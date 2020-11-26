---
uid: Microsoft.Quantum.Canon.ApplyIfZero
title: Applyif Zero-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZero
qsharp.summary: Applies an operation conditioned on a classical result value being zero.
ms.openlocfilehash: 3b14ef8a1aa736fe096a21fe51be5a7c5bb1d09d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209432"
---
# <a name="applyifzero-operation"></a><span data-ttu-id="21c7f-102">Applyif Zero-Vorgang</span><span class="sxs-lookup"><span data-stu-id="21c7f-102">ApplyIfZero operation</span></span>

<span data-ttu-id="21c7f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="21c7f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="21c7f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="21c7f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="21c7f-105">Wendet einen Vorgang an, der von einem klassischen Ergebniswert von 0 (null) abhängt.</span><span class="sxs-lookup"><span data-stu-id="21c7f-105">Applies an operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZero<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="21c7f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21c7f-106">Description</span></span>

<span data-ttu-id="21c7f-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `Zero` .</span><span class="sxs-lookup"><span data-stu-id="21c7f-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="21c7f-108">Gibt `One` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="21c7f-108">If `One`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="21c7f-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="21c7f-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="21c7f-110">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="21c7f-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="21c7f-111">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="21c7f-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="21c7f-112">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="21c7f-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="21c7f-113">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21c7f-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="21c7f-114">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="21c7f-114">target : 'T</span></span>

<span data-ttu-id="21c7f-115">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="21c7f-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="21c7f-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="21c7f-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="21c7f-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="21c7f-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="21c7f-118">GIF</span><span class="sxs-lookup"><span data-stu-id="21c7f-118">'T</span></span>

<span data-ttu-id="21c7f-119">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21c7f-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="21c7f-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21c7f-120">See Also</span></span>

- [<span data-ttu-id="21c7f-121">Microsoft. Quantum. Canon. applyif zeroc</span><span class="sxs-lookup"><span data-stu-id="21c7f-121">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="21c7f-122">Microsoft. Quantum. Canon. applyif zeroa</span><span class="sxs-lookup"><span data-stu-id="21c7f-122">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="21c7f-123">Microsoft. Quantum. Canon. applyif nuloca</span><span class="sxs-lookup"><span data-stu-id="21c7f-123">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)