---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Applydeelementc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: c8d7841e3846ab435671f7959c724f987d8ad5a0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217576"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="8a261-102">Applydeelementc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8a261-102">ApplyToElementC operation</span></span>

<span data-ttu-id="8a261-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8a261-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8a261-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8a261-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8a261-105">Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="8a261-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="8a261-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a261-106">Description</span></span>

<span data-ttu-id="8a261-107">Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="8a261-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="8a261-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a261-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="8a261-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="8a261-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="8a261-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8a261-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="8a261-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8a261-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8a261-112">Ein Index in das Array von Zielen.</span><span class="sxs-lookup"><span data-stu-id="8a261-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="8a261-113">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="8a261-113">targets : 'T[]</span></span>

<span data-ttu-id="8a261-114">Ein Array möglicher Ziele für `op` .</span><span class="sxs-lookup"><span data-stu-id="8a261-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8a261-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8a261-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8a261-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8a261-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8a261-117">GIF</span><span class="sxs-lookup"><span data-stu-id="8a261-117">'T</span></span>

<span data-ttu-id="8a261-118">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a261-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a261-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8a261-119">See Also</span></span>

- [<span data-ttu-id="8a261-120">Microsoft. Quantum. Canon. applyyelement</span><span class="sxs-lookup"><span data-stu-id="8a261-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="8a261-121">Microsoft. Quantum. Canon. applyyelementa</span><span class="sxs-lookup"><span data-stu-id="8a261-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="8a261-122">Microsoft. Quantum. Canon. applyyelementca</span><span class="sxs-lookup"><span data-stu-id="8a261-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)