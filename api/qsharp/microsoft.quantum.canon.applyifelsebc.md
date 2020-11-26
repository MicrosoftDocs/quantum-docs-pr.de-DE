---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: Applyifeleinbc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: ea06b0a0a07659407e13caa2baa4f3e37ca2a0f7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209518"
---
# <a name="applyifelsebc-operation"></a><span data-ttu-id="3644f-102">Applyifeleinbc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3644f-102">ApplyIfElseBC operation</span></span>

<span data-ttu-id="3644f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3644f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3644f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3644f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3644f-105">Wendet je nach dem Wert eines klassischen Bits einen von zwei kontrollierbaren Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="3644f-105">Applies one of two controllable operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="3644f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3644f-106">Description</span></span>

<span data-ttu-id="3644f-107">Wenn ein Bit angegeben ist `bit` , wendet den Vorgang `trueOp` mit `trueInput` als Eingabe an, wenn den Wert `bit` `true` hat, und gilt, wenn den Wert hat `falseOp(falseInput)` `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="3644f-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="3644f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3644f-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="3644f-109">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3644f-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3644f-110">Der boolesche Wert, der verwendet wird, um zu bestimmen, ob `trueOp` oder `falseOp` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="3644f-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit--is-ctl"></a><span data-ttu-id="3644f-111">trueop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="3644f-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="3644f-112">Der zu verwendende kontrollierbare Vorgang, wenn `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="3644f-112">The controllable operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="3644f-113">trueinput: 't</span><span class="sxs-lookup"><span data-stu-id="3644f-113">trueInput : 'T</span></span>

<span data-ttu-id="3644f-114">Die Eingabe, die für bereitgestellt werden soll, `trueOp` Wenn `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="3644f-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit--is-ctl"></a><span data-ttu-id="3644f-115">falseop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="3644f-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="3644f-116">Der zu verwendende kontrollierbare Vorgang, wenn `bit` ist `false` .</span><span class="sxs-lookup"><span data-stu-id="3644f-116">The controllable operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="3644f-117">falseinput: ' U</span><span class="sxs-lookup"><span data-stu-id="3644f-117">falseInput : 'U</span></span>

<span data-ttu-id="3644f-118">Die Eingabe, die für bereitgestellt werden soll, `falseOp` Wenn `bit` ist `false` .</span><span class="sxs-lookup"><span data-stu-id="3644f-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3644f-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3644f-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3644f-120">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3644f-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3644f-121">GIF</span><span class="sxs-lookup"><span data-stu-id="3644f-121">'T</span></span>

<span data-ttu-id="3644f-122">Der Eingabetyp des Vorgangs `trueOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3644f-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="3644f-123">"U</span><span class="sxs-lookup"><span data-stu-id="3644f-123">'U</span></span>

<span data-ttu-id="3644f-124">Der Eingabetyp des Vorgangs `falseOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3644f-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="3644f-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3644f-125">See Also</span></span>

- [<span data-ttu-id="3644f-126">Microsoft. Quantum. Canon. applyif Zero</span><span class="sxs-lookup"><span data-stu-id="3644f-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="3644f-127">Microsoft. Quantum. Canon. applyifone</span><span class="sxs-lookup"><span data-stu-id="3644f-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="3644f-128">Microsoft. Quantum. Canon. applyifelserc</span><span class="sxs-lookup"><span data-stu-id="3644f-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="3644f-129">Microsoft. Quantum. Canon. applyifelsera</span><span class="sxs-lookup"><span data-stu-id="3644f-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="3644f-130">Microsoft. Quantum. Canon. applyifelserca</span><span class="sxs-lookup"><span data-stu-id="3644f-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)