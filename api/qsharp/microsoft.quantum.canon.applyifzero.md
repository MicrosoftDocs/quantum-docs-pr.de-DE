---
uid: Microsoft.Quantum.Canon.ApplyIfZero
title: Applyif Zero-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZero
qsharp.summary: Applies an operation conditioned on a classical result value being zero.
ms.openlocfilehash: 215b71a8d2e4f8a22df05b210824bc40a969b6f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841742"
---
# <a name="applyifzero-operation"></a><span data-ttu-id="c8e34-102">Applyif Zero-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c8e34-102">ApplyIfZero operation</span></span>

<span data-ttu-id="c8e34-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c8e34-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c8e34-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c8e34-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c8e34-105">Wendet einen Vorgang an, der von einem klassischen Ergebniswert von 0 (null) abhängt.</span><span class="sxs-lookup"><span data-stu-id="c8e34-105">Applies an operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZero<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="c8e34-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8e34-106">Description</span></span>

<span data-ttu-id="c8e34-107">Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `Zero` .</span><span class="sxs-lookup"><span data-stu-id="c8e34-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="c8e34-108">Gibt `One` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="c8e34-108">If `One`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="c8e34-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8e34-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="c8e34-110">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="c8e34-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="c8e34-111">Ein Messergebnis, das steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8e34-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="c8e34-112">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c8e34-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c8e34-113">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8e34-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="c8e34-114">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="c8e34-114">target : 'T</span></span>

<span data-ttu-id="c8e34-115">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8e34-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c8e34-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c8e34-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c8e34-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c8e34-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c8e34-118">GIF</span><span class="sxs-lookup"><span data-stu-id="c8e34-118">'T</span></span>

<span data-ttu-id="c8e34-119">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8e34-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8e34-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8e34-120">See Also</span></span>

- [<span data-ttu-id="c8e34-121">Microsoft. Quantum. Canon. applyif zeroc</span><span class="sxs-lookup"><span data-stu-id="c8e34-121">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="c8e34-122">Microsoft. Quantum. Canon. applyif zeroa</span><span class="sxs-lookup"><span data-stu-id="c8e34-122">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="c8e34-123">Microsoft. Quantum. Canon. applyif nuloca</span><span class="sxs-lookup"><span data-stu-id="c8e34-123">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)