---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Applydeheadca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 1bb24006a2d52167dfc7a7871cfbf5a4378d1cb7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850618"
---
# <a name="applytoheadca-operation"></a><span data-ttu-id="3131e-102">Applydeheadca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3131e-102">ApplyToHeadCA operation</span></span>

<span data-ttu-id="3131e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3131e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3131e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3131e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3131e-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="3131e-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="3131e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3131e-106">Description</span></span>

<span data-ttu-id="3131e-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="3131e-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="3131e-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3131e-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="3131e-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="3131e-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3131e-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="3131e-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="3131e-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="3131e-111">targets : 'T[]</span></span>

<span data-ttu-id="3131e-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="3131e-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3131e-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3131e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3131e-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3131e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3131e-115">GIF</span><span class="sxs-lookup"><span data-stu-id="3131e-115">'T</span></span>

<span data-ttu-id="3131e-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3131e-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="3131e-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3131e-117">See Also</span></span>

- [<span data-ttu-id="3131e-118">Microsoft. Quantum. Canon. applyyhead</span><span class="sxs-lookup"><span data-stu-id="3131e-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="3131e-119">Microsoft. Quantum. Canon. applyumheada</span><span class="sxs-lookup"><span data-stu-id="3131e-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="3131e-120">Microsoft. Quantum. Canon. applyumheadc</span><span class="sxs-lookup"><span data-stu-id="3131e-120">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)