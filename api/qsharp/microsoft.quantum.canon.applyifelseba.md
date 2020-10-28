---
uid: Microsoft.Quantum.Canon.ApplyIfElseBA
title: Applyifeltba-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBA
qsharp.summary: Applies one of two adjointable operations, depending on the value of a classical bit.
ms.openlocfilehash: ce08907646c3210f76244f29aa0d936e2bd6ee43
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705330"
---
# <a name="applyifelseba-operation"></a><span data-ttu-id="0eb4a-102">Applyifeltba-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0eb4a-102">ApplyIfElseBA operation</span></span>

<span data-ttu-id="0eb4a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0eb4a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0eb4a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0eb4a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0eb4a-105">Wendet abhängig vom Wert eines klassischen Bits einen von zwei adjointable-Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="0eb4a-105">Applies one of two adjointable operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj), trueInput : 'T), (falseOp : ('U => Unit is Adj), falseInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="0eb4a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0eb4a-106">Description</span></span>

<span data-ttu-id="0eb4a-107">Wenn ein Bit angegeben ist `bit` , wendet den Vorgang `trueOp` mit `trueInput` als Eingabe an, wenn den Wert `bit` `true` hat, und gilt, wenn den Wert hat `falseOp(falseInput)` `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="0eb4a-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="0eb4a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0eb4a-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="0eb4a-109">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0eb4a-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0eb4a-110">Der boolesche Wert, der verwendet wird, um zu bestimmen, ob `trueOp` oder `falseOp` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0eb4a-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit-adj"></a><span data-ttu-id="0eb4a-111">trueop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="0eb4a-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="0eb4a-112">Der adjointable-Vorgang, der angewendet werden soll, wenn `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="0eb4a-112">The adjointable operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="0eb4a-113">trueinput: 't</span><span class="sxs-lookup"><span data-stu-id="0eb4a-113">trueInput : 'T</span></span>

<span data-ttu-id="0eb4a-114">Die Eingabe, die für bereitgestellt werden soll, `trueOp` Wenn `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="0eb4a-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit-adj"></a><span data-ttu-id="0eb4a-115">falseop: "U => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="0eb4a-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="0eb4a-116">Der adjointable-Vorgang, der angewendet werden soll, wenn `bit` ist `false` .</span><span class="sxs-lookup"><span data-stu-id="0eb4a-116">The adjointable operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="0eb4a-117">falseinput: ' U</span><span class="sxs-lookup"><span data-stu-id="0eb4a-117">falseInput : 'U</span></span>

<span data-ttu-id="0eb4a-118">Die Eingabe, die für bereitgestellt werden soll, `falseOp` Wenn `bit` ist `false` .</span><span class="sxs-lookup"><span data-stu-id="0eb4a-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0eb4a-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0eb4a-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0eb4a-120">Typparameter</span><span class="sxs-lookup"><span data-stu-id="0eb4a-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0eb4a-121">GIF</span><span class="sxs-lookup"><span data-stu-id="0eb4a-121">'T</span></span>

<span data-ttu-id="0eb4a-122">Der Eingabetyp des Vorgangs `trueOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0eb4a-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="0eb4a-123">"U</span><span class="sxs-lookup"><span data-stu-id="0eb4a-123">'U</span></span>

<span data-ttu-id="0eb4a-124">Der Eingabetyp des Vorgangs `falseOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0eb4a-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="0eb4a-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0eb4a-125">See Also</span></span>

- [<span data-ttu-id="0eb4a-126">Microsoft. Quantum. Canon. applyif Zero</span><span class="sxs-lookup"><span data-stu-id="0eb4a-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="0eb4a-127">Microsoft. Quantum. Canon. applyifone</span><span class="sxs-lookup"><span data-stu-id="0eb4a-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="0eb4a-128">Microsoft. Quantum. Canon. applyifelserc</span><span class="sxs-lookup"><span data-stu-id="0eb4a-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="0eb4a-129">Microsoft. Quantum. Canon. applyifelsera</span><span class="sxs-lookup"><span data-stu-id="0eb4a-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="0eb4a-130">Microsoft. Quantum. Canon. applyifelserca</span><span class="sxs-lookup"><span data-stu-id="0eb4a-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)