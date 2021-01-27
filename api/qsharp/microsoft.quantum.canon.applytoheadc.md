---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Applydeheadc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3a65ad52e0b2f8b3a921fc549c35311f24d0e189
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850629"
---
# <a name="applytoheadc-operation"></a><span data-ttu-id="21ed1-102">Applydeheadc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="21ed1-102">ApplyToHeadC operation</span></span>

<span data-ttu-id="21ed1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="21ed1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="21ed1-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="21ed1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="21ed1-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="21ed1-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="21ed1-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21ed1-106">Description</span></span>

<span data-ttu-id="21ed1-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="21ed1-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="21ed1-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="21ed1-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="21ed1-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="21ed1-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="21ed1-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="21ed1-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="21ed1-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="21ed1-111">targets : 'T[]</span></span>

<span data-ttu-id="21ed1-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="21ed1-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="21ed1-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="21ed1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="21ed1-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="21ed1-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="21ed1-115">GIF</span><span class="sxs-lookup"><span data-stu-id="21ed1-115">'T</span></span>

<span data-ttu-id="21ed1-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21ed1-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="21ed1-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21ed1-117">See Also</span></span>

- [<span data-ttu-id="21ed1-118">Microsoft. Quantum. Canon. applyyhead</span><span class="sxs-lookup"><span data-stu-id="21ed1-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="21ed1-119">Microsoft. Quantum. Canon. applyumheada</span><span class="sxs-lookup"><span data-stu-id="21ed1-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="21ed1-120">Microsoft. Quantum. Canon. ApplyTo headca</span><span class="sxs-lookup"><span data-stu-id="21ed1-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)