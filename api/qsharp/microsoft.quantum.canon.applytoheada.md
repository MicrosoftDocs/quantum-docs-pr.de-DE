---
uid: Microsoft.Quantum.Canon.ApplyToHeadA
title: Applydeheada-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 290347ff54492c4291db540e82cedcdd822a354e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850643"
---
# <a name="applytoheada-operation"></a><span data-ttu-id="f5f6f-102">Applydeheada-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f5f6f-102">ApplyToHeadA operation</span></span>

<span data-ttu-id="f5f6f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f5f6f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f5f6f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f5f6f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f5f6f-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="f5f6f-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="f5f6f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5f6f-106">Description</span></span>

<span data-ttu-id="f5f6f-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="f5f6f-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="f5f6f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5f6f-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="f5f6f-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="f5f6f-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="f5f6f-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f5f6f-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="f5f6f-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="f5f6f-111">targets : 'T[]</span></span>

<span data-ttu-id="f5f6f-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="f5f6f-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f5f6f-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f5f6f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f5f6f-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f5f6f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f5f6f-115">GIF</span><span class="sxs-lookup"><span data-stu-id="f5f6f-115">'T</span></span>

<span data-ttu-id="f5f6f-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5f6f-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5f6f-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f5f6f-117">See Also</span></span>

- [<span data-ttu-id="f5f6f-118">Microsoft. Quantum. Canon. applyyhead</span><span class="sxs-lookup"><span data-stu-id="f5f6f-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="f5f6f-119">Microsoft. Quantum. Canon. applyumheadc</span><span class="sxs-lookup"><span data-stu-id="f5f6f-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="f5f6f-120">Microsoft. Quantum. Canon. ApplyTo headca</span><span class="sxs-lookup"><span data-stu-id="f5f6f-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)