---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Applydehead-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 4e5fc439f48a5c7e527b7805c35cce18eca3ab36
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704799"
---
# <a name="applytohead-operation"></a><span data-ttu-id="feaa4-102">Applydehead-Vorgang</span><span class="sxs-lookup"><span data-stu-id="feaa4-102">ApplyToHead operation</span></span>

<span data-ttu-id="feaa4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="feaa4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="feaa4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="feaa4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="feaa4-105">Wendet einen Vorgang auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="feaa4-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="feaa4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="feaa4-106">Description</span></span>

<span data-ttu-id="feaa4-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="feaa4-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="feaa4-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="feaa4-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="feaa4-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="feaa4-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="feaa4-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="feaa4-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="feaa4-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="feaa4-111">targets : 'T[]</span></span>

<span data-ttu-id="feaa4-112">Ein Array von Zielen, von dem die erste angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="feaa4-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="feaa4-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="feaa4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="feaa4-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="feaa4-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="feaa4-115">GIF</span><span class="sxs-lookup"><span data-stu-id="feaa4-115">'T</span></span>

<span data-ttu-id="feaa4-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="feaa4-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="feaa4-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="feaa4-117">See Also</span></span>

- [<span data-ttu-id="feaa4-118">Microsoft. Quantum. Canon. applyumheada</span><span class="sxs-lookup"><span data-stu-id="feaa4-118">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="feaa4-119">Microsoft. Quantum. Canon. applyumheadc</span><span class="sxs-lookup"><span data-stu-id="feaa4-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="feaa4-120">Microsoft. Quantum. Canon. ApplyTo headca</span><span class="sxs-lookup"><span data-stu-id="feaa4-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)