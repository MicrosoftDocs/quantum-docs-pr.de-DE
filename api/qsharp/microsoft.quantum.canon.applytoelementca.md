---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: Applydeelementca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 420a92ae10d2fc260024968b1846e669c4b62d73
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841469"
---
# <a name="applytoelementca-operation"></a><span data-ttu-id="14c8f-102">Applydeelementca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="14c8f-102">ApplyToElementCA operation</span></span>

<span data-ttu-id="14c8f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="14c8f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="14c8f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="14c8f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="14c8f-105">Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="14c8f-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="14c8f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14c8f-106">Description</span></span>

<span data-ttu-id="14c8f-107">Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="14c8f-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="14c8f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14c8f-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="14c8f-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="14c8f-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="14c8f-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="14c8f-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="14c8f-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="14c8f-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="14c8f-112">Ein Index in das Array von Zielen.</span><span class="sxs-lookup"><span data-stu-id="14c8f-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="14c8f-113">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="14c8f-113">targets : 'T[]</span></span>

<span data-ttu-id="14c8f-114">Ein Array möglicher Ziele für `op` .</span><span class="sxs-lookup"><span data-stu-id="14c8f-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="14c8f-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="14c8f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="14c8f-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="14c8f-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="14c8f-117">GIF</span><span class="sxs-lookup"><span data-stu-id="14c8f-117">'T</span></span>

<span data-ttu-id="14c8f-118">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14c8f-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="14c8f-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14c8f-119">See Also</span></span>

- [<span data-ttu-id="14c8f-120">Microsoft. Quantum. Canon. applyyelement</span><span class="sxs-lookup"><span data-stu-id="14c8f-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="14c8f-121">Microsoft. Quantum. Canon. applyyelementc</span><span class="sxs-lookup"><span data-stu-id="14c8f-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="14c8f-122">Microsoft. Quantum. Canon. applyyelementa</span><span class="sxs-lookup"><span data-stu-id="14c8f-122">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)