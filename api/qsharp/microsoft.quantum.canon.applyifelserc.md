---
uid: Microsoft.Quantum.Canon.ApplyIfElseRC
title: Applyifelserc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical result.
ms.openlocfilehash: 45bd0f46fb2e28c5c9aaa21cb7ec065baf279d2a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705282"
---
# <a name="applyifelserc-operation"></a><span data-ttu-id="2aaf2-102">Applyifelserc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2aaf2-102">ApplyIfElseRC operation</span></span>

<span data-ttu-id="2aaf2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2aaf2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2aaf2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2aaf2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2aaf2-105">Wendet je nach dem Wert eines klassischen Ergebnisses einen von zwei kontrollierbaren Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="2aaf2-105">Applies one of two controllable operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRC<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Ctl), oneInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="2aaf2-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2aaf2-106">Description</span></span>

<span data-ttu-id="2aaf2-107">Bei einem Ergebnis `result` wendet den Vorgang `zeroOp` mit `zeroInput` als Eingabe an, wenn `result` gleich ist `Zero` , und gilt, wenn gleich ist `oneOp(oneInput)` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="2aaf2-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="2aaf2-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2aaf2-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="2aaf2-109">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="2aaf2-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="2aaf2-110">Das Messergebnis, mit dem bestimmt wird, ob `zeroOp` oder `oneOp` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2aaf2-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit-ctl"></a><span data-ttu-id="2aaf2-111">zeroop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="2aaf2-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="2aaf2-112">Der zu verwendende kontrollierbare Vorgang, wenn `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="2aaf2-112">The controllable operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="2aaf2-113">NULL-Eingabe: 't</span><span class="sxs-lookup"><span data-stu-id="2aaf2-113">zeroInput : 'T</span></span>

<span data-ttu-id="2aaf2-114">Die Eingabe, die für bereitgestellt werden soll `zeroOp` `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="2aaf2-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit-ctl"></a><span data-ttu-id="2aaf2-115">oneop: "U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="2aaf2-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="2aaf2-116">Der zu verwendende kontrollierbare Vorgang, wenn `result == One` .</span><span class="sxs-lookup"><span data-stu-id="2aaf2-116">The controllable operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="2aaf2-117">oneinput: ' U</span><span class="sxs-lookup"><span data-stu-id="2aaf2-117">oneInput : 'U</span></span>

<span data-ttu-id="2aaf2-118">Die Eingabe, die für bereitgestellt werden soll `oneOp` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="2aaf2-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2aaf2-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2aaf2-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2aaf2-120">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2aaf2-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2aaf2-121">GIF</span><span class="sxs-lookup"><span data-stu-id="2aaf2-121">'T</span></span>

<span data-ttu-id="2aaf2-122">Der Eingabetyp des Vorgangs `zeroOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2aaf2-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="2aaf2-123">"U</span><span class="sxs-lookup"><span data-stu-id="2aaf2-123">'U</span></span>

<span data-ttu-id="2aaf2-124">Der Eingabetyp des Vorgangs `oneOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2aaf2-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2aaf2-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2aaf2-125">See Also</span></span>

- [<span data-ttu-id="2aaf2-126">Microsoft. Quantum. Canon. applyif Zero</span><span class="sxs-lookup"><span data-stu-id="2aaf2-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="2aaf2-127">Microsoft. Quantum. Canon. applyifone</span><span class="sxs-lookup"><span data-stu-id="2aaf2-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="2aaf2-128">Microsoft. Quantum. Canon. applyifelserc</span><span class="sxs-lookup"><span data-stu-id="2aaf2-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="2aaf2-129">Microsoft. Quantum. Canon. applyifelsera</span><span class="sxs-lookup"><span data-stu-id="2aaf2-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="2aaf2-130">Microsoft. Quantum. Canon. applyifelserca</span><span class="sxs-lookup"><span data-stu-id="2aaf2-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)