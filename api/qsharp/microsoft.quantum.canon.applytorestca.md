---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Applyorestca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 3123c7f7b5e5c7f5cb17a34eedc81b3912109883
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208158"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="a49c5-102">Applyorestca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a49c5-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="a49c5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a49c5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a49c5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a49c5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a49c5-105">Wendet einen Vorgang auf alle außer auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="a49c5-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a49c5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a49c5-106">Description</span></span>

<span data-ttu-id="a49c5-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="a49c5-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="a49c5-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a49c5-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="a49c5-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="a49c5-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a49c5-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a49c5-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="a49c5-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="a49c5-111">targets : 'T[]</span></span>

<span data-ttu-id="a49c5-112">Ein Array von Zielen, von denen alle außer der ersten übernommen werden `op` .</span><span class="sxs-lookup"><span data-stu-id="a49c5-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a49c5-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a49c5-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a49c5-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a49c5-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a49c5-115">GIF</span><span class="sxs-lookup"><span data-stu-id="a49c5-115">'T</span></span>

<span data-ttu-id="a49c5-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a49c5-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a49c5-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a49c5-117">See Also</span></span>

- [<span data-ttu-id="a49c5-118">Microsoft. Quantum. Canon. applytor EST</span><span class="sxs-lookup"><span data-stu-id="a49c5-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="a49c5-119">Microsoft. Quantum. Canon. applytoriesta</span><span class="sxs-lookup"><span data-stu-id="a49c5-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="a49c5-120">Microsoft. Quantum. Canon. applytor</span><span class="sxs-lookup"><span data-stu-id="a49c5-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)