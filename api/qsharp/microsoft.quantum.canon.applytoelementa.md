---
uid: Microsoft.Quantum.Canon.ApplyToElementA
title: Applyyelementa-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 57d870c7fbd099212b13f75bd85e57c046280d73
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850770"
---
# <a name="applytoelementa-operation"></a><span data-ttu-id="2319a-102">Applyyelementa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2319a-102">ApplyToElementA operation</span></span>

<span data-ttu-id="2319a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2319a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2319a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2319a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2319a-105">Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="2319a-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementA<'T> (op : ('T => Unit is Adj), index : Int, targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="2319a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2319a-106">Description</span></span>

<span data-ttu-id="2319a-107">Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="2319a-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="2319a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2319a-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="2319a-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="2319a-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="2319a-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2319a-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="2319a-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2319a-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2319a-112">Ein Index in das Array von Zielen.</span><span class="sxs-lookup"><span data-stu-id="2319a-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="2319a-113">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="2319a-113">targets : 'T[]</span></span>

<span data-ttu-id="2319a-114">Ein Array möglicher Ziele für `op` .</span><span class="sxs-lookup"><span data-stu-id="2319a-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2319a-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2319a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2319a-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2319a-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2319a-117">GIF</span><span class="sxs-lookup"><span data-stu-id="2319a-117">'T</span></span>

<span data-ttu-id="2319a-118">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2319a-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2319a-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2319a-119">See Also</span></span>

- [<span data-ttu-id="2319a-120">Microsoft. Quantum. Canon. applyyelement</span><span class="sxs-lookup"><span data-stu-id="2319a-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="2319a-121">Microsoft. Quantum. Canon. applyyelementc</span><span class="sxs-lookup"><span data-stu-id="2319a-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="2319a-122">Microsoft. Quantum. Canon. applyyelementca</span><span class="sxs-lookup"><span data-stu-id="2319a-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)