---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Applydeheadca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: f28cff599e06090145fac860dbaf8274c966f80a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208549"
---
# <a name="applytoheadca-operation"></a><span data-ttu-id="642c4-102">Applydeheadca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="642c4-102">ApplyToHeadCA operation</span></span>

<span data-ttu-id="642c4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="642c4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="642c4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="642c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="642c4-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="642c4-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="642c4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="642c4-106">Description</span></span>

<span data-ttu-id="642c4-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="642c4-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="642c4-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="642c4-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="642c4-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="642c4-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="642c4-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="642c4-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="642c4-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="642c4-111">targets : 'T[]</span></span>

<span data-ttu-id="642c4-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="642c4-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="642c4-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="642c4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="642c4-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="642c4-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="642c4-115">GIF</span><span class="sxs-lookup"><span data-stu-id="642c4-115">'T</span></span>

<span data-ttu-id="642c4-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="642c4-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="642c4-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="642c4-117">See Also</span></span>

- [<span data-ttu-id="642c4-118">Microsoft. Quantum. Canon. applyyhead</span><span class="sxs-lookup"><span data-stu-id="642c4-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="642c4-119">Microsoft. Quantum. Canon. applyumheada</span><span class="sxs-lookup"><span data-stu-id="642c4-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="642c4-120">Microsoft. Quantum. Canon. applyumheadc</span><span class="sxs-lookup"><span data-stu-id="642c4-120">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)