---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: Applyifca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: 9057c79622f15a082963d94fc261664e00322feb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705351"
---
# <a name="applyifca-operation"></a><span data-ttu-id="c27f5-102">Applyifca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c27f5-102">ApplyIfCA operation</span></span>

<span data-ttu-id="c27f5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c27f5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c27f5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c27f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c27f5-105">Wendet einen einheitlichen Vorgang an, der auf einem klassischen Bit bedingt ist.</span><span class="sxs-lookup"><span data-stu-id="c27f5-105">Applies a unitary operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="c27f5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c27f5-106">Description</span></span>

<span data-ttu-id="c27f5-107">Bei einem Vorgang `op` und einem Bitwert `bit` gilt für `op` das, `target` wenn gleich `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="c27f5-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="c27f5-108">Gibt `false` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="c27f5-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="c27f5-109">Das-Suffix `CA` gibt an, dass der anzuwendende Vorgang einheitlich (steuerbar und adjointable) ist.</span><span class="sxs-lookup"><span data-stu-id="c27f5-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="c27f5-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c27f5-110">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="c27f5-111">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="c27f5-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="c27f5-112">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c27f5-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="c27f5-113">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c27f5-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c27f5-114">ein boolescher Wert, der steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c27f5-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="c27f5-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="c27f5-115">target : 'T</span></span>

<span data-ttu-id="c27f5-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c27f5-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c27f5-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c27f5-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c27f5-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c27f5-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c27f5-119">GIF</span><span class="sxs-lookup"><span data-stu-id="c27f5-119">'T</span></span>

<span data-ttu-id="c27f5-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c27f5-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="c27f5-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c27f5-121">See Also</span></span>

- [<span data-ttu-id="c27f5-122">Microsoft. Quantum. Canon. applyifc</span><span class="sxs-lookup"><span data-stu-id="c27f5-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="c27f5-123">Microsoft. Quantum. Canon. applyifa</span><span class="sxs-lookup"><span data-stu-id="c27f5-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="c27f5-124">Microsoft. Quantum. Canon. applyifca</span><span class="sxs-lookup"><span data-stu-id="c27f5-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)