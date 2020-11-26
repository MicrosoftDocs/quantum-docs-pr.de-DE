---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: Applyifa-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: d2880bbb95ebaf621ef9e5885051b94f32a3f1cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218766"
---
# <a name="applyifa-operation"></a><span data-ttu-id="e4a93-102">Applyifa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e4a93-102">ApplyIfA operation</span></span>

<span data-ttu-id="e4a93-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e4a93-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e4a93-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e4a93-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e4a93-105">Wendet einen adjointable-Vorgang an, der auf einem klassischen Bit bedingt ist.</span><span class="sxs-lookup"><span data-stu-id="e4a93-105">Applies a adjointable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="e4a93-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4a93-106">Description</span></span>

<span data-ttu-id="e4a93-107">Bei einem Vorgang `op` und einem Bitwert `bit` gilt für `op` das, `target` wenn gleich `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="e4a93-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="e4a93-108">Gibt `false` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="e4a93-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="e4a93-109">Das-Suffix `A` gibt an, dass der anzuwendende Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="e4a93-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="e4a93-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e4a93-110">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="e4a93-111">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="e4a93-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e4a93-112">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4a93-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="e4a93-113">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e4a93-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e4a93-114">ein boolescher Wert, der steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4a93-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="e4a93-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="e4a93-115">target : 'T</span></span>

<span data-ttu-id="e4a93-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4a93-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e4a93-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e4a93-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e4a93-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e4a93-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e4a93-119">GIF</span><span class="sxs-lookup"><span data-stu-id="e4a93-119">'T</span></span>

<span data-ttu-id="e4a93-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4a93-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4a93-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4a93-121">See Also</span></span>

- [<span data-ttu-id="e4a93-122">Microsoft. Quantum. Canon. applyifc</span><span class="sxs-lookup"><span data-stu-id="e4a93-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="e4a93-123">Microsoft. Quantum. Canon. applyifa</span><span class="sxs-lookup"><span data-stu-id="e4a93-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="e4a93-124">Microsoft. Quantum. Canon. applyifca</span><span class="sxs-lookup"><span data-stu-id="e4a93-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)