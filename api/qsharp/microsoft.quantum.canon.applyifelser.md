---
uid: Microsoft.Quantum.Canon.ApplyIfElseR
title: Applyifelser-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseR
qsharp.summary: Applies one of two operations, depending on the value of a classical result.
ms.openlocfilehash: 874dae2ba5e842066e9c1582af431a73520e4ccd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209535"
---
# <a name="applyifelser-operation"></a><span data-ttu-id="560d4-102">Applyifelser-Vorgang</span><span class="sxs-lookup"><span data-stu-id="560d4-102">ApplyIfElseR operation</span></span>

<span data-ttu-id="560d4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="560d4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="560d4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="560d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="560d4-105">Wendet je nach dem Wert eines klassischen Ergebnisses einen von zwei Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="560d4-105">Applies one of two operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseR<'T, 'U> (result : Result, (zeroOp : ('T => Unit), zeroInput : 'T), (oneOp : ('U => Unit), oneInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="560d4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="560d4-106">Description</span></span>

<span data-ttu-id="560d4-107">Bei einem Ergebnis `result` wendet den Vorgang `zeroOp` mit `zeroInput` als Eingabe an, wenn `result` gleich ist `Zero` , und gilt, wenn gleich ist `oneOp(oneInput)` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="560d4-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="560d4-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="560d4-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="560d4-109">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="560d4-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="560d4-110">Das Messergebnis, mit dem bestimmt wird, ob `zeroOp` oder `oneOp` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="560d4-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit"></a><span data-ttu-id="560d4-111">zeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="560d4-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="560d4-112">Der Vorgang, der angewendet werden soll, wenn `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="560d4-112">The operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="560d4-113">NULL-Eingabe: 't</span><span class="sxs-lookup"><span data-stu-id="560d4-113">zeroInput : 'T</span></span>

<span data-ttu-id="560d4-114">Die Eingabe, die für bereitgestellt werden soll `zeroOp` `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="560d4-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit"></a><span data-ttu-id="560d4-115">oneop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="560d4-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="560d4-116">Der Vorgang, der angewendet werden soll, wenn `result == One` .</span><span class="sxs-lookup"><span data-stu-id="560d4-116">The operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="560d4-117">oneinput: ' U</span><span class="sxs-lookup"><span data-stu-id="560d4-117">oneInput : 'U</span></span>

<span data-ttu-id="560d4-118">Die Eingabe, die für bereitgestellt werden soll `oneOp` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="560d4-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="560d4-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="560d4-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="560d4-120">Typparameter</span><span class="sxs-lookup"><span data-stu-id="560d4-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="560d4-121">GIF</span><span class="sxs-lookup"><span data-stu-id="560d4-121">'T</span></span>

<span data-ttu-id="560d4-122">Der Eingabetyp des Vorgangs `zeroOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="560d4-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="560d4-123">"U</span><span class="sxs-lookup"><span data-stu-id="560d4-123">'U</span></span>

<span data-ttu-id="560d4-124">Der Eingabetyp des Vorgangs `oneOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="560d4-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="560d4-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="560d4-125">See Also</span></span>

- [<span data-ttu-id="560d4-126">Microsoft. Quantum. Canon. applyif Zero</span><span class="sxs-lookup"><span data-stu-id="560d4-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="560d4-127">Microsoft. Quantum. Canon. applyifone</span><span class="sxs-lookup"><span data-stu-id="560d4-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="560d4-128">Microsoft. Quantum. Canon. applyifelserc</span><span class="sxs-lookup"><span data-stu-id="560d4-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="560d4-129">Microsoft. Quantum. Canon. applyifelsera</span><span class="sxs-lookup"><span data-stu-id="560d4-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="560d4-130">Microsoft. Quantum. Canon. applyifelserca</span><span class="sxs-lookup"><span data-stu-id="560d4-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)