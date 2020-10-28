---
uid: Microsoft.Quantum.Canon.ApplyToHeadA
title: Applydeheada-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: ba060243cb01782fd8529e0b05ee7258a66314f5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704791"
---
# <a name="applytoheada-operation"></a><span data-ttu-id="6468f-102">Applydeheada-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6468f-102">ApplyToHeadA operation</span></span>

<span data-ttu-id="6468f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6468f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6468f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6468f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6468f-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="6468f-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="6468f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6468f-106">Description</span></span>

<span data-ttu-id="6468f-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="6468f-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="6468f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6468f-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="6468f-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="6468f-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="6468f-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6468f-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="6468f-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="6468f-111">targets : 'T[]</span></span>

<span data-ttu-id="6468f-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="6468f-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6468f-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6468f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6468f-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="6468f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6468f-115">GIF</span><span class="sxs-lookup"><span data-stu-id="6468f-115">'T</span></span>

<span data-ttu-id="6468f-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6468f-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="6468f-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6468f-117">See Also</span></span>

- [<span data-ttu-id="6468f-118">Microsoft. Quantum. Canon. applyyhead</span><span class="sxs-lookup"><span data-stu-id="6468f-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="6468f-119">Microsoft. Quantum. Canon. applyumheadc</span><span class="sxs-lookup"><span data-stu-id="6468f-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="6468f-120">Microsoft. Quantum. Canon. ApplyTo headca</span><span class="sxs-lookup"><span data-stu-id="6468f-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)