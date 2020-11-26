---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: Applydeelement-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 8cbc42a1c43b4c9a037729671eb3c82d365af580
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217626"
---
# <a name="applytoelement-operation"></a><span data-ttu-id="ed6cd-102">Applydeelement-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ed6cd-102">ApplyToElement operation</span></span>

<span data-ttu-id="ed6cd-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ed6cd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ed6cd-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ed6cd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ed6cd-105">Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="ed6cd-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="ed6cd-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed6cd-106">Description</span></span>

<span data-ttu-id="ed6cd-107">Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="ed6cd-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="ed6cd-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ed6cd-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="ed6cd-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed6cd-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ed6cd-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ed6cd-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="ed6cd-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ed6cd-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ed6cd-112">Ein Index in das Array von Zielen.</span><span class="sxs-lookup"><span data-stu-id="ed6cd-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ed6cd-113">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="ed6cd-113">targets : 'T[]</span></span>

<span data-ttu-id="ed6cd-114">Ein Array möglicher Ziele für `op` .</span><span class="sxs-lookup"><span data-stu-id="ed6cd-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ed6cd-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed6cd-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ed6cd-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ed6cd-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ed6cd-117">GIF</span><span class="sxs-lookup"><span data-stu-id="ed6cd-117">'T</span></span>

<span data-ttu-id="ed6cd-118">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed6cd-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed6cd-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed6cd-119">See Also</span></span>

- [<span data-ttu-id="ed6cd-120">Microsoft. Quantum. Canon. applyyelementc</span><span class="sxs-lookup"><span data-stu-id="ed6cd-120">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="ed6cd-121">Microsoft. Quantum. Canon. applyyelementa</span><span class="sxs-lookup"><span data-stu-id="ed6cd-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="ed6cd-122">Microsoft. Quantum. Canon. applyyelementca</span><span class="sxs-lookup"><span data-stu-id="ed6cd-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)