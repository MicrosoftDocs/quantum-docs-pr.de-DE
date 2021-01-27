---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: Applydeelement-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 5159eee07f7398cc6194c9907a37b78a63aaf263
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850778"
---
# <a name="applytoelement-operation"></a><span data-ttu-id="0c3b9-102">Applydeelement-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0c3b9-102">ApplyToElement operation</span></span>

<span data-ttu-id="0c3b9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0c3b9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0c3b9-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0c3b9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0c3b9-105">Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="0c3b9-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="0c3b9-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c3b9-106">Description</span></span>

<span data-ttu-id="0c3b9-107">Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="0c3b9-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="0c3b9-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c3b9-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="0c3b9-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0c3b9-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="0c3b9-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0c3b9-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="0c3b9-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0c3b9-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0c3b9-112">Ein Index in das Array von Zielen.</span><span class="sxs-lookup"><span data-stu-id="0c3b9-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="0c3b9-113">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="0c3b9-113">targets : 'T[]</span></span>

<span data-ttu-id="0c3b9-114">Ein Array möglicher Ziele für `op` .</span><span class="sxs-lookup"><span data-stu-id="0c3b9-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0c3b9-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0c3b9-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0c3b9-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="0c3b9-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0c3b9-117">GIF</span><span class="sxs-lookup"><span data-stu-id="0c3b9-117">'T</span></span>

<span data-ttu-id="0c3b9-118">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c3b9-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c3b9-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0c3b9-119">See Also</span></span>

- [<span data-ttu-id="0c3b9-120">Microsoft. Quantum. Canon. applyyelementc</span><span class="sxs-lookup"><span data-stu-id="0c3b9-120">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="0c3b9-121">Microsoft. Quantum. Canon. applyyelementa</span><span class="sxs-lookup"><span data-stu-id="0c3b9-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="0c3b9-122">Microsoft. Quantum. Canon. applyyelementca</span><span class="sxs-lookup"><span data-stu-id="0c3b9-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)