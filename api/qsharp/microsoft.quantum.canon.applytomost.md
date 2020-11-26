---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: Applytomost-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 7e7824b431ccff644cf5cc53145163327eb8ad36
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208532"
---
# <a name="applytomost-operation"></a><span data-ttu-id="16070-102">Applytomost-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16070-102">ApplyToMost operation</span></span>

<span data-ttu-id="16070-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="16070-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="16070-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="16070-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="16070-105">Wendet einen Vorgang auf alle bis auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="16070-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="16070-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16070-106">Description</span></span>

<span data-ttu-id="16070-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="16070-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="16070-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="16070-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="16070-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16070-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="16070-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="16070-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="16070-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="16070-111">targets : 'T[]</span></span>

<span data-ttu-id="16070-112">Ein Array von Zielen, von denen alle außer der letzten angewendet werden `op` .</span><span class="sxs-lookup"><span data-stu-id="16070-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="16070-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16070-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="16070-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="16070-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="16070-115">GIF</span><span class="sxs-lookup"><span data-stu-id="16070-115">'T</span></span>

<span data-ttu-id="16070-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16070-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="16070-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="16070-117">See Also</span></span>

- [<span data-ttu-id="16070-118">Microsoft. Quantum. Canon. applytomosta</span><span class="sxs-lookup"><span data-stu-id="16070-118">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="16070-119">Microsoft. Quantum. Canon. applytomostc</span><span class="sxs-lookup"><span data-stu-id="16070-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="16070-120">Microsoft. Quantum. Canon. applytomostca</span><span class="sxs-lookup"><span data-stu-id="16070-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)