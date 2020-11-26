---
uid: Microsoft.Quantum.Canon.ApplyIfElseRCA
title: Applyifelserca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical result.
ms.openlocfilehash: dfd1c16a25a2da507024813a380386c8f4e49d30
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218749"
---
# <a name="applyifelserca-operation"></a><span data-ttu-id="f4be8-102">Applyifelserca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f4be8-102">ApplyIfElseRCA operation</span></span>

<span data-ttu-id="f4be8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f4be8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f4be8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f4be8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f4be8-105">Wendet abhängig vom Wert eines klassischen Ergebnisses einen von zwei einheitlichen Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="f4be8-105">Applies one of two unitary operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRCA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj + Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Adj + Ctl), oneInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="f4be8-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4be8-106">Description</span></span>

<span data-ttu-id="f4be8-107">Bei einem Ergebnis `result` wendet den Vorgang `zeroOp` mit `zeroInput` als Eingabe an, wenn `result` gleich ist `Zero` , und gilt, wenn gleich ist `oneOp(oneInput)` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="f4be8-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="f4be8-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f4be8-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="f4be8-109">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="f4be8-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="f4be8-110">Das Messergebnis, mit dem bestimmt wird, ob `zeroOp` oder `oneOp` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4be8-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit--is-adj--ctl"></a><span data-ttu-id="f4be8-111">zeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="f4be8-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f4be8-112">Der einheitliche Vorgang, der angewendet werden soll, wenn `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="f4be8-112">The unitary operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="f4be8-113">NULL-Eingabe: 't</span><span class="sxs-lookup"><span data-stu-id="f4be8-113">zeroInput : 'T</span></span>

<span data-ttu-id="f4be8-114">Die Eingabe, die für bereitgestellt werden soll `zeroOp` `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="f4be8-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit--is-adj--ctl"></a><span data-ttu-id="f4be8-115">oneop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="f4be8-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f4be8-116">Der einheitliche Vorgang, der angewendet werden soll, wenn `result == One` .</span><span class="sxs-lookup"><span data-stu-id="f4be8-116">The unitary operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="f4be8-117">oneinput: ' U</span><span class="sxs-lookup"><span data-stu-id="f4be8-117">oneInput : 'U</span></span>

<span data-ttu-id="f4be8-118">Die Eingabe, die für bereitgestellt werden soll `oneOp` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="f4be8-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f4be8-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f4be8-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f4be8-120">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f4be8-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f4be8-121">GIF</span><span class="sxs-lookup"><span data-stu-id="f4be8-121">'T</span></span>

<span data-ttu-id="f4be8-122">Der Eingabetyp des Vorgangs `zeroOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4be8-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="f4be8-123">"U</span><span class="sxs-lookup"><span data-stu-id="f4be8-123">'U</span></span>

<span data-ttu-id="f4be8-124">Der Eingabetyp des Vorgangs `oneOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4be8-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4be8-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f4be8-125">See Also</span></span>

- [<span data-ttu-id="f4be8-126">Microsoft. Quantum. Canon. applyif Zero</span><span class="sxs-lookup"><span data-stu-id="f4be8-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="f4be8-127">Microsoft. Quantum. Canon. applyifone</span><span class="sxs-lookup"><span data-stu-id="f4be8-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="f4be8-128">Microsoft. Quantum. Canon. applyifelserc</span><span class="sxs-lookup"><span data-stu-id="f4be8-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="f4be8-129">Microsoft. Quantum. Canon. applyifelsera</span><span class="sxs-lookup"><span data-stu-id="f4be8-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="f4be8-130">Microsoft. Quantum. Canon. applyifelserca</span><span class="sxs-lookup"><span data-stu-id="f4be8-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)