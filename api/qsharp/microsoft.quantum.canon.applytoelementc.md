---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Applydeelementc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: bd466ff59e6e962be9a7e58b6d298c60b0d1d90d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704903"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="f7000-102">Applydeelementc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f7000-102">ApplyToElementC operation</span></span>

<span data-ttu-id="f7000-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f7000-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f7000-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f7000-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f7000-105">Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="f7000-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="f7000-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7000-106">Description</span></span>

<span data-ttu-id="f7000-107">Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="f7000-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="f7000-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7000-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="f7000-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="f7000-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="f7000-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f7000-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="f7000-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f7000-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f7000-112">Ein Index in das Array von Zielen.</span><span class="sxs-lookup"><span data-stu-id="f7000-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="f7000-113">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="f7000-113">targets : 'T[]</span></span>

<span data-ttu-id="f7000-114">Ein Array möglicher Ziele für `op` .</span><span class="sxs-lookup"><span data-stu-id="f7000-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f7000-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f7000-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f7000-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f7000-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f7000-117">GIF</span><span class="sxs-lookup"><span data-stu-id="f7000-117">'T</span></span>

<span data-ttu-id="f7000-118">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7000-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7000-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f7000-119">See Also</span></span>

- [<span data-ttu-id="f7000-120">Microsoft. Quantum. Canon. applyyelement</span><span class="sxs-lookup"><span data-stu-id="f7000-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="f7000-121">Microsoft. Quantum. Canon. applyyelementa</span><span class="sxs-lookup"><span data-stu-id="f7000-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="f7000-122">Microsoft. Quantum. Canon. applyyelementca</span><span class="sxs-lookup"><span data-stu-id="f7000-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)