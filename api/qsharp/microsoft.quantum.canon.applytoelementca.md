---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: Applydeelementca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 8ae4ece0d3d56ea2be1ce494ab0c5ee7caacbbf8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208855"
---
# <a name="applytoelementca-operation"></a><span data-ttu-id="37218-102">Applydeelementca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="37218-102">ApplyToElementCA operation</span></span>

<span data-ttu-id="37218-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="37218-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="37218-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="37218-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="37218-105">Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="37218-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="37218-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37218-106">Description</span></span>

<span data-ttu-id="37218-107">Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="37218-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="37218-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="37218-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="37218-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="37218-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="37218-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="37218-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="37218-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="37218-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="37218-112">Ein Index in das Array von Zielen.</span><span class="sxs-lookup"><span data-stu-id="37218-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="37218-113">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="37218-113">targets : 'T[]</span></span>

<span data-ttu-id="37218-114">Ein Array möglicher Ziele für `op` .</span><span class="sxs-lookup"><span data-stu-id="37218-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="37218-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="37218-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="37218-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="37218-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37218-117">GIF</span><span class="sxs-lookup"><span data-stu-id="37218-117">'T</span></span>

<span data-ttu-id="37218-118">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37218-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="37218-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="37218-119">See Also</span></span>

- [<span data-ttu-id="37218-120">Microsoft. Quantum. Canon. applyyelement</span><span class="sxs-lookup"><span data-stu-id="37218-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="37218-121">Microsoft. Quantum. Canon. applyyelementc</span><span class="sxs-lookup"><span data-stu-id="37218-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="37218-122">Microsoft. Quantum. Canon. applyyelementa</span><span class="sxs-lookup"><span data-stu-id="37218-122">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)