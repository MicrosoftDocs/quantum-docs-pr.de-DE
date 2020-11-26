---
uid: Microsoft.Quantum.Canon.ApplyIfElseRA
title: Applyifelsera-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRA
qsharp.summary: Applies one of two adjointable operations, depending on the value of a classical result.
ms.openlocfilehash: 3ebd09b1e5876ff397f3524ba828ba26a271e91e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218596"
---
# <a name="applyifelsera-operation"></a><span data-ttu-id="2bc11-102">Applyifelsera-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2bc11-102">ApplyIfElseRA operation</span></span>

<span data-ttu-id="2bc11-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2bc11-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2bc11-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2bc11-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2bc11-105">Wendet abhängig vom Wert eines klassischen Ergebnisses einen von zwei adjointable-Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="2bc11-105">Applies one of two adjointable operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj), zeroInput : 'T), (oneOp : ('U => Unit is Adj), oneInput : 'U)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="2bc11-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bc11-106">Description</span></span>

<span data-ttu-id="2bc11-107">Bei einem Ergebnis `result` wendet den Vorgang `zeroOp` mit `zeroInput` als Eingabe an, wenn `result` gleich ist `Zero` , und gilt, wenn gleich ist `oneOp(oneInput)` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="2bc11-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="2bc11-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2bc11-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="2bc11-109">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="2bc11-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="2bc11-110">Das Messergebnis, mit dem bestimmt wird, ob `zeroOp` oder `oneOp` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2bc11-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit--is-adj"></a><span data-ttu-id="2bc11-111">zeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="2bc11-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="2bc11-112">Der adjointable-Vorgang, der angewendet werden soll, wenn `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="2bc11-112">The adjointable operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="2bc11-113">NULL-Eingabe: 't</span><span class="sxs-lookup"><span data-stu-id="2bc11-113">zeroInput : 'T</span></span>

<span data-ttu-id="2bc11-114">Die Eingabe, die für bereitgestellt werden soll `zeroOp` `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="2bc11-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit--is-adj"></a><span data-ttu-id="2bc11-115">oneop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="2bc11-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="2bc11-116">Der adjointable-Vorgang, der angewendet werden soll, wenn `result == One` .</span><span class="sxs-lookup"><span data-stu-id="2bc11-116">The adjointable operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="2bc11-117">oneinput: ' U</span><span class="sxs-lookup"><span data-stu-id="2bc11-117">oneInput : 'U</span></span>

<span data-ttu-id="2bc11-118">Die Eingabe, die für bereitgestellt werden soll `oneOp` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="2bc11-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2bc11-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2bc11-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2bc11-120">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2bc11-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2bc11-121">GIF</span><span class="sxs-lookup"><span data-stu-id="2bc11-121">'T</span></span>

<span data-ttu-id="2bc11-122">Der Eingabetyp des Vorgangs `zeroOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2bc11-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="2bc11-123">"U</span><span class="sxs-lookup"><span data-stu-id="2bc11-123">'U</span></span>

<span data-ttu-id="2bc11-124">Der Eingabetyp des Vorgangs `oneOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2bc11-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bc11-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2bc11-125">See Also</span></span>

- [<span data-ttu-id="2bc11-126">Microsoft. Quantum. Canon. applyif Zero</span><span class="sxs-lookup"><span data-stu-id="2bc11-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="2bc11-127">Microsoft. Quantum. Canon. applyifone</span><span class="sxs-lookup"><span data-stu-id="2bc11-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="2bc11-128">Microsoft. Quantum. Canon. applyifelserc</span><span class="sxs-lookup"><span data-stu-id="2bc11-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="2bc11-129">Microsoft. Quantum. Canon. applyifelsera</span><span class="sxs-lookup"><span data-stu-id="2bc11-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="2bc11-130">Microsoft. Quantum. Canon. applyifelserca</span><span class="sxs-lookup"><span data-stu-id="2bc11-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)