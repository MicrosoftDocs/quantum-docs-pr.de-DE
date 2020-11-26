---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Applydeheadc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 2b7321a6c385e2d98a0e91a8f58091ea8dc43ff4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208600"
---
# <a name="applytoheadc-operation"></a><span data-ttu-id="21d11-102">Applydeheadc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="21d11-102">ApplyToHeadC operation</span></span>

<span data-ttu-id="21d11-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="21d11-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="21d11-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="21d11-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="21d11-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="21d11-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="21d11-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21d11-106">Description</span></span>

<span data-ttu-id="21d11-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="21d11-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="21d11-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="21d11-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="21d11-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="21d11-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="21d11-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="21d11-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="21d11-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="21d11-111">targets : 'T[]</span></span>

<span data-ttu-id="21d11-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="21d11-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="21d11-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="21d11-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="21d11-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="21d11-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="21d11-115">GIF</span><span class="sxs-lookup"><span data-stu-id="21d11-115">'T</span></span>

<span data-ttu-id="21d11-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21d11-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="21d11-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21d11-117">See Also</span></span>

- [<span data-ttu-id="21d11-118">Microsoft. Quantum. Canon. applyyhead</span><span class="sxs-lookup"><span data-stu-id="21d11-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="21d11-119">Microsoft. Quantum. Canon. applyumheada</span><span class="sxs-lookup"><span data-stu-id="21d11-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="21d11-120">Microsoft. Quantum. Canon. ApplyTo headca</span><span class="sxs-lookup"><span data-stu-id="21d11-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)