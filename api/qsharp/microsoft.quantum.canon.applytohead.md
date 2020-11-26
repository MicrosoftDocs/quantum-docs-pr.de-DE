---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Applydehead-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 35f19cbb1090e974e18f338239764c9c8b854116
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217338"
---
# <a name="applytohead-operation"></a><span data-ttu-id="52f8e-102">Applydehead-Vorgang</span><span class="sxs-lookup"><span data-stu-id="52f8e-102">ApplyToHead operation</span></span>

<span data-ttu-id="52f8e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="52f8e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="52f8e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="52f8e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="52f8e-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="52f8e-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="52f8e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52f8e-106">Description</span></span>

<span data-ttu-id="52f8e-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="52f8e-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="52f8e-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="52f8e-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="52f8e-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52f8e-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="52f8e-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="52f8e-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="52f8e-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="52f8e-111">targets : 'T[]</span></span>

<span data-ttu-id="52f8e-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="52f8e-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="52f8e-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52f8e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="52f8e-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="52f8e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="52f8e-115">GIF</span><span class="sxs-lookup"><span data-stu-id="52f8e-115">'T</span></span>

<span data-ttu-id="52f8e-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52f8e-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="52f8e-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="52f8e-117">See Also</span></span>

- [<span data-ttu-id="52f8e-118">Microsoft. Quantum. Canon. applyumheada</span><span class="sxs-lookup"><span data-stu-id="52f8e-118">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="52f8e-119">Microsoft. Quantum. Canon. applyumheadc</span><span class="sxs-lookup"><span data-stu-id="52f8e-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="52f8e-120">Microsoft. Quantum. Canon. ApplyTo headca</span><span class="sxs-lookup"><span data-stu-id="52f8e-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)