---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Applydeheadc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3ff6c25837f1219dd456bf1739a2953ff72e2df9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704786"
---
# <a name="applytoheadc-operation"></a><span data-ttu-id="19ec3-102">Applydeheadc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="19ec3-102">ApplyToHeadC operation</span></span>

<span data-ttu-id="19ec3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="19ec3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="19ec3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="19ec3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="19ec3-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="19ec3-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="19ec3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19ec3-106">Description</span></span>

<span data-ttu-id="19ec3-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="19ec3-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="19ec3-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19ec3-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="19ec3-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="19ec3-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="19ec3-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="19ec3-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="19ec3-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="19ec3-111">targets : 'T[]</span></span>

<span data-ttu-id="19ec3-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="19ec3-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="19ec3-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="19ec3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="19ec3-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="19ec3-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="19ec3-115">GIF</span><span class="sxs-lookup"><span data-stu-id="19ec3-115">'T</span></span>

<span data-ttu-id="19ec3-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="19ec3-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="19ec3-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="19ec3-117">See Also</span></span>

- [<span data-ttu-id="19ec3-118">Microsoft. Quantum. Canon. applyyhead</span><span class="sxs-lookup"><span data-stu-id="19ec3-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="19ec3-119">Microsoft. Quantum. Canon. applyumheada</span><span class="sxs-lookup"><span data-stu-id="19ec3-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="19ec3-120">Microsoft. Quantum. Canon. ApplyTo headca</span><span class="sxs-lookup"><span data-stu-id="19ec3-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)