---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Applyifc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: e16254154909eb844164538acb7b82fedc11f86a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705354"
---
# <a name="applyifc-operation"></a><span data-ttu-id="dff79-102">Applyifc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dff79-102">ApplyIfC operation</span></span>

<span data-ttu-id="dff79-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dff79-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dff79-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dff79-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dff79-105">Wendet eine steuerbare Operation an, die auf einem klassischen Bit bedingt ist.</span><span class="sxs-lookup"><span data-stu-id="dff79-105">Applies a controllable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="dff79-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dff79-106">Description</span></span>

<span data-ttu-id="dff79-107">Bei einem Vorgang `op` und einem Bitwert `bit` gilt für `op` das, `target` wenn gleich `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="dff79-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="dff79-108">Gibt `false` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="dff79-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="dff79-109">Das-Suffix `C` gibt an, dass der anzuwendende Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="dff79-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="dff79-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dff79-110">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="dff79-111">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="dff79-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="dff79-112">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dff79-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="dff79-113">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="dff79-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="dff79-114">ein boolescher Wert, der steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dff79-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="dff79-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="dff79-115">target : 'T</span></span>

<span data-ttu-id="dff79-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dff79-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dff79-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dff79-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dff79-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="dff79-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dff79-119">GIF</span><span class="sxs-lookup"><span data-stu-id="dff79-119">'T</span></span>

<span data-ttu-id="dff79-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dff79-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="dff79-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dff79-121">See Also</span></span>

- [<span data-ttu-id="dff79-122">Microsoft. Quantum. Canon. applyifc</span><span class="sxs-lookup"><span data-stu-id="dff79-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="dff79-123">Microsoft. Quantum. Canon. applyifa</span><span class="sxs-lookup"><span data-stu-id="dff79-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="dff79-124">Microsoft. Quantum. Canon. applyifca</span><span class="sxs-lookup"><span data-stu-id="dff79-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)