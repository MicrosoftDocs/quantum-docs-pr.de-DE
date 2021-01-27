---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: Applyifeleinbc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: 6140a8382cbd00589d1aef99e004f71f5d9295a9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841817"
---
# <a name="applyifelsebc-operation"></a><span data-ttu-id="1460d-102">Applyifeleinbc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1460d-102">ApplyIfElseBC operation</span></span>

<span data-ttu-id="1460d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1460d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1460d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1460d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1460d-105">Wendet je nach dem Wert eines klassischen Bits einen von zwei kontrollierbaren Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="1460d-105">Applies one of two controllable operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="1460d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1460d-106">Description</span></span>

<span data-ttu-id="1460d-107">Wenn ein Bit angegeben ist `bit` , wendet den Vorgang `trueOp` mit `trueInput` als Eingabe an, wenn den Wert `bit` `true` hat, und gilt, wenn den Wert hat `falseOp(falseInput)` `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="1460d-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="1460d-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1460d-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="1460d-109">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1460d-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1460d-110">Der boolesche Wert, der verwendet wird, um zu bestimmen, ob `trueOp` oder `falseOp` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1460d-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit--is-ctl"></a><span data-ttu-id="1460d-111">trueop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="1460d-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="1460d-112">Der zu verwendende kontrollierbare Vorgang, wenn `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="1460d-112">The controllable operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="1460d-113">trueinput: 't</span><span class="sxs-lookup"><span data-stu-id="1460d-113">trueInput : 'T</span></span>

<span data-ttu-id="1460d-114">Die Eingabe, die für bereitgestellt werden soll, `trueOp` Wenn `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="1460d-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit--is-ctl"></a><span data-ttu-id="1460d-115">falseop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="1460d-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="1460d-116">Der zu verwendende kontrollierbare Vorgang, wenn `bit` ist `false` .</span><span class="sxs-lookup"><span data-stu-id="1460d-116">The controllable operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="1460d-117">falseinput: ' U</span><span class="sxs-lookup"><span data-stu-id="1460d-117">falseInput : 'U</span></span>

<span data-ttu-id="1460d-118">Die Eingabe, die für bereitgestellt werden soll, `falseOp` Wenn `bit` ist `false` .</span><span class="sxs-lookup"><span data-stu-id="1460d-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1460d-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1460d-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1460d-120">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1460d-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1460d-121">GIF</span><span class="sxs-lookup"><span data-stu-id="1460d-121">'T</span></span>

<span data-ttu-id="1460d-122">Der Eingabetyp des Vorgangs `trueOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1460d-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="1460d-123">"U</span><span class="sxs-lookup"><span data-stu-id="1460d-123">'U</span></span>

<span data-ttu-id="1460d-124">Der Eingabetyp des Vorgangs `falseOp` , der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1460d-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="1460d-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1460d-125">See Also</span></span>

- [<span data-ttu-id="1460d-126">Microsoft. Quantum. Canon. applyif Zero</span><span class="sxs-lookup"><span data-stu-id="1460d-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="1460d-127">Microsoft. Quantum. Canon. applyifone</span><span class="sxs-lookup"><span data-stu-id="1460d-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="1460d-128">Microsoft. Quantum. Canon. applyifelserc</span><span class="sxs-lookup"><span data-stu-id="1460d-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="1460d-129">Microsoft. Quantum. Canon. applyifelsera</span><span class="sxs-lookup"><span data-stu-id="1460d-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="1460d-130">Microsoft. Quantum. Canon. applyifelserca</span><span class="sxs-lookup"><span data-stu-id="1460d-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)