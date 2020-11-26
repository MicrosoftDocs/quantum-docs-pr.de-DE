---
uid: Microsoft.Quantum.Canon.ApplyToElementA
title: Applyyelementa-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: e8318a7873476ee49d8e1e235e6c917a38ee6200
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208872"
---
# <a name="applytoelementa-operation"></a><span data-ttu-id="a6961-102">Applyyelementa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a6961-102">ApplyToElementA operation</span></span>

<span data-ttu-id="a6961-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a6961-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a6961-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a6961-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a6961-105">Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="a6961-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementA<'T> (op : ('T => Unit is Adj), index : Int, targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="a6961-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6961-106">Description</span></span>

<span data-ttu-id="a6961-107">Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="a6961-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="a6961-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a6961-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="a6961-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="a6961-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a6961-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a6961-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="a6961-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a6961-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a6961-112">Ein Index in das Array von Zielen.</span><span class="sxs-lookup"><span data-stu-id="a6961-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="a6961-113">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="a6961-113">targets : 'T[]</span></span>

<span data-ttu-id="a6961-114">Ein Array möglicher Ziele für `op` .</span><span class="sxs-lookup"><span data-stu-id="a6961-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a6961-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a6961-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a6961-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a6961-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a6961-117">GIF</span><span class="sxs-lookup"><span data-stu-id="a6961-117">'T</span></span>

<span data-ttu-id="a6961-118">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6961-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6961-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a6961-119">See Also</span></span>

- [<span data-ttu-id="a6961-120">Microsoft. Quantum. Canon. applyyelement</span><span class="sxs-lookup"><span data-stu-id="a6961-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="a6961-121">Microsoft. Quantum. Canon. applyyelementc</span><span class="sxs-lookup"><span data-stu-id="a6961-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="a6961-122">Microsoft. Quantum. Canon. applyyelementca</span><span class="sxs-lookup"><span data-stu-id="a6961-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)