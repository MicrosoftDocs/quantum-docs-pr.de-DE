---
uid: Microsoft.Quantum.Canon.ApplyToRest
title: Applytor-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRest
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 29bf080d693c668421181f10faef50f5681683be
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704706"
---
# <a name="applytorest-operation"></a><span data-ttu-id="79693-102">Applytor-Vorgang</span><span class="sxs-lookup"><span data-stu-id="79693-102">ApplyToRest operation</span></span>

<span data-ttu-id="79693-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="79693-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="79693-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="79693-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="79693-105">Wendet einen Vorgang auf alle außer auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="79693-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRest<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="79693-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79693-106">Description</span></span>

<span data-ttu-id="79693-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="79693-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="79693-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="79693-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="79693-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79693-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="79693-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="79693-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="79693-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="79693-111">targets : 'T[]</span></span>

<span data-ttu-id="79693-112">Ein Array von Zielen, von denen alle außer der ersten übernommen werden `op` .</span><span class="sxs-lookup"><span data-stu-id="79693-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="79693-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79693-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="79693-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="79693-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="79693-115">GIF</span><span class="sxs-lookup"><span data-stu-id="79693-115">'T</span></span>

<span data-ttu-id="79693-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="79693-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="79693-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="79693-117">See Also</span></span>

- [<span data-ttu-id="79693-118">Microsoft. Quantum. Canon. applytoriesta</span><span class="sxs-lookup"><span data-stu-id="79693-118">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="79693-119">Microsoft. Quantum. Canon. applytor</span><span class="sxs-lookup"><span data-stu-id="79693-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="79693-120">Microsoft. Quantum. Canon. applytor estca</span><span class="sxs-lookup"><span data-stu-id="79693-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)