---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Applyif-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c8f6860a7a3b8af86b0edb048baccbf057dd245a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705359"
---
# <a name="applyif-operation"></a><span data-ttu-id="585f6-102">Applyif-Vorgang</span><span class="sxs-lookup"><span data-stu-id="585f6-102">ApplyIf operation</span></span>

<span data-ttu-id="585f6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="585f6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="585f6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="585f6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="585f6-105">Wendet einen Vorgang an, der von einem klassischen Bit abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="585f6-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="585f6-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="585f6-106">Description</span></span>

<span data-ttu-id="585f6-107">Bei einem Vorgang `op` und einem Bitwert `bit` gilt für `op` das, `target` wenn gleich `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="585f6-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="585f6-108">Gibt `false` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="585f6-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="585f6-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="585f6-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="585f6-110">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="585f6-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="585f6-111">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="585f6-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="585f6-112">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="585f6-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="585f6-113">ein boolescher Wert, der steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="585f6-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="585f6-114">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="585f6-114">target : 'T</span></span>

<span data-ttu-id="585f6-115">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="585f6-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="585f6-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="585f6-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="585f6-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="585f6-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="585f6-118">GIF</span><span class="sxs-lookup"><span data-stu-id="585f6-118">'T</span></span>

<span data-ttu-id="585f6-119">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="585f6-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="585f6-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="585f6-120">See Also</span></span>

- [<span data-ttu-id="585f6-121">Microsoft. Quantum. Canon. applyifc</span><span class="sxs-lookup"><span data-stu-id="585f6-121">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="585f6-122">Microsoft. Quantum. Canon. applyifa</span><span class="sxs-lookup"><span data-stu-id="585f6-122">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="585f6-123">Microsoft. Quantum. Canon. applyifca</span><span class="sxs-lookup"><span data-stu-id="585f6-123">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)