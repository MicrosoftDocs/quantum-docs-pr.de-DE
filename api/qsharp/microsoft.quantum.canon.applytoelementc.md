---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Applydeelementc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: bc63b6b591781a6283b872ef0c2509094a656b4c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850743"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="adc9f-102">Applydeelementc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="adc9f-102">ApplyToElementC operation</span></span>

<span data-ttu-id="adc9f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="adc9f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="adc9f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="adc9f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="adc9f-105">Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="adc9f-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="adc9f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adc9f-106">Description</span></span>

<span data-ttu-id="adc9f-107">Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="adc9f-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="adc9f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="adc9f-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="adc9f-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="adc9f-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="adc9f-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="adc9f-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="adc9f-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="adc9f-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="adc9f-112">Ein Index in das Array von Zielen.</span><span class="sxs-lookup"><span data-stu-id="adc9f-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="adc9f-113">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="adc9f-113">targets : 'T[]</span></span>

<span data-ttu-id="adc9f-114">Ein Array möglicher Ziele für `op` .</span><span class="sxs-lookup"><span data-stu-id="adc9f-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="adc9f-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="adc9f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="adc9f-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="adc9f-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="adc9f-117">GIF</span><span class="sxs-lookup"><span data-stu-id="adc9f-117">'T</span></span>

<span data-ttu-id="adc9f-118">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="adc9f-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="adc9f-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="adc9f-119">See Also</span></span>

- [<span data-ttu-id="adc9f-120">Microsoft. Quantum. Canon. applyyelement</span><span class="sxs-lookup"><span data-stu-id="adc9f-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="adc9f-121">Microsoft. Quantum. Canon. applyyelementa</span><span class="sxs-lookup"><span data-stu-id="adc9f-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="adc9f-122">Microsoft. Quantum. Canon. applyyelementca</span><span class="sxs-lookup"><span data-stu-id="adc9f-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)