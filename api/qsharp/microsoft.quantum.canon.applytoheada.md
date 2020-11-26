---
uid: Microsoft.Quantum.Canon.ApplyToHeadA
title: Applydeheada-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3397c059706c48ff8ca47dd2312cfa9565aacaba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208634"
---
# <a name="applytoheada-operation"></a><span data-ttu-id="184e8-102">Applydeheada-Vorgang</span><span class="sxs-lookup"><span data-stu-id="184e8-102">ApplyToHeadA operation</span></span>

<span data-ttu-id="184e8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="184e8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="184e8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="184e8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="184e8-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="184e8-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="184e8-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="184e8-106">Description</span></span>

<span data-ttu-id="184e8-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="184e8-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="184e8-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="184e8-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="184e8-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="184e8-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="184e8-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="184e8-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="184e8-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="184e8-111">targets : 'T[]</span></span>

<span data-ttu-id="184e8-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="184e8-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="184e8-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="184e8-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="184e8-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="184e8-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="184e8-115">GIF</span><span class="sxs-lookup"><span data-stu-id="184e8-115">'T</span></span>

<span data-ttu-id="184e8-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="184e8-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="184e8-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="184e8-117">See Also</span></span>

- [<span data-ttu-id="184e8-118">Microsoft. Quantum. Canon. applyyhead</span><span class="sxs-lookup"><span data-stu-id="184e8-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="184e8-119">Microsoft. Quantum. Canon. applyumheadc</span><span class="sxs-lookup"><span data-stu-id="184e8-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="184e8-120">Microsoft. Quantum. Canon. ApplyTo headca</span><span class="sxs-lookup"><span data-stu-id="184e8-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)