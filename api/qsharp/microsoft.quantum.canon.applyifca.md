---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: Applyifca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: b0ac469d6dea51951e0d9b2cfceb54253d4b4c5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209620"
---
# <a name="applyifca-operation"></a><span data-ttu-id="0183b-102">Applyifca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0183b-102">ApplyIfCA operation</span></span>

<span data-ttu-id="0183b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0183b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0183b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0183b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0183b-105">Wendet einen einheitlichen Vorgang an, der auf einem klassischen Bit bedingt ist.</span><span class="sxs-lookup"><span data-stu-id="0183b-105">Applies a unitary operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="0183b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0183b-106">Description</span></span>

<span data-ttu-id="0183b-107">Bei einem Vorgang `op` und einem Bitwert `bit` gilt für `op` das, `target` wenn gleich `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="0183b-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="0183b-108">Gibt `false` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="0183b-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="0183b-109">Das-Suffix `CA` gibt an, dass der anzuwendende Vorgang einheitlich (steuerbar und adjointable) ist.</span><span class="sxs-lookup"><span data-stu-id="0183b-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="0183b-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0183b-110">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="0183b-111">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="0183b-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="0183b-112">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0183b-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="0183b-113">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0183b-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0183b-114">ein boolescher Wert, der steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0183b-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="0183b-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="0183b-115">target : 'T</span></span>

<span data-ttu-id="0183b-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0183b-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0183b-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0183b-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0183b-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="0183b-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0183b-119">GIF</span><span class="sxs-lookup"><span data-stu-id="0183b-119">'T</span></span>

<span data-ttu-id="0183b-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0183b-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="0183b-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0183b-121">See Also</span></span>

- [<span data-ttu-id="0183b-122">Microsoft. Quantum. Canon. applyifc</span><span class="sxs-lookup"><span data-stu-id="0183b-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="0183b-123">Microsoft. Quantum. Canon. applyifa</span><span class="sxs-lookup"><span data-stu-id="0183b-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="0183b-124">Microsoft. Quantum. Canon. applyifca</span><span class="sxs-lookup"><span data-stu-id="0183b-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)