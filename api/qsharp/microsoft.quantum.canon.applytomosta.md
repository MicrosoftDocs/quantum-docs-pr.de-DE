---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Applytomosta-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 994cada2952809dc84a70b76dc4ede8286c89855
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704762"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="cb7a1-102">Applytomosta-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cb7a1-102">ApplyToMostA operation</span></span>

<span data-ttu-id="cb7a1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cb7a1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cb7a1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cb7a1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cb7a1-105">Wendet einen Vorgang auf alle bis auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="cb7a1-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="cb7a1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb7a1-106">Description</span></span>

<span data-ttu-id="cb7a1-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="cb7a1-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="cb7a1-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cb7a1-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="cb7a1-109">OP: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="cb7a1-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="cb7a1-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cb7a1-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="cb7a1-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="cb7a1-111">targets : 'T[]</span></span>

<span data-ttu-id="cb7a1-112">Ein Array von Zielen, von denen alle außer der letzten angewendet werden `op` .</span><span class="sxs-lookup"><span data-stu-id="cb7a1-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cb7a1-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cb7a1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cb7a1-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="cb7a1-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cb7a1-115">GIF</span><span class="sxs-lookup"><span data-stu-id="cb7a1-115">'T</span></span>

<span data-ttu-id="cb7a1-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb7a1-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb7a1-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cb7a1-117">See Also</span></span>

- [<span data-ttu-id="cb7a1-118">Microsoft. Quantum. Canon. applytomost</span><span class="sxs-lookup"><span data-stu-id="cb7a1-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="cb7a1-119">Microsoft. Quantum. Canon. applytomostc</span><span class="sxs-lookup"><span data-stu-id="cb7a1-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="cb7a1-120">Microsoft. Quantum. Canon. applytomostca</span><span class="sxs-lookup"><span data-stu-id="cb7a1-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)