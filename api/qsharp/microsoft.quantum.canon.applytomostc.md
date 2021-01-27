---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Applytomostc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 14de9f367aa7d19f64f13186d402239ae1fef3c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850558"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="523d8-102">Applytomostc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="523d8-102">ApplyToMostC operation</span></span>

<span data-ttu-id="523d8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="523d8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="523d8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="523d8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="523d8-105">Wendet einen Vorgang auf alle bis auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="523d8-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="523d8-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="523d8-106">Description</span></span>

<span data-ttu-id="523d8-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="523d8-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="523d8-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="523d8-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="523d8-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="523d8-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="523d8-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="523d8-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="523d8-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="523d8-111">targets : 'T[]</span></span>

<span data-ttu-id="523d8-112">Ein Array von Zielen, von denen alle außer der letzten angewendet werden `op` .</span><span class="sxs-lookup"><span data-stu-id="523d8-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="523d8-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="523d8-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="523d8-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="523d8-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="523d8-115">GIF</span><span class="sxs-lookup"><span data-stu-id="523d8-115">'T</span></span>

<span data-ttu-id="523d8-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="523d8-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="523d8-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="523d8-117">See Also</span></span>

- [<span data-ttu-id="523d8-118">Microsoft. Quantum. Canon. applytomost</span><span class="sxs-lookup"><span data-stu-id="523d8-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="523d8-119">Microsoft. Quantum. Canon. applytomosta</span><span class="sxs-lookup"><span data-stu-id="523d8-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="523d8-120">Microsoft. Quantum. Canon. applytomostca</span><span class="sxs-lookup"><span data-stu-id="523d8-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)