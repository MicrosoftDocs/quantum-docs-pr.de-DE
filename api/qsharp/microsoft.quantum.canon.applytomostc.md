---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Applytomostc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: af55093e44ce023c9e8b7e478730f4c527cf6d32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208464"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="85c12-102">Applytomostc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="85c12-102">ApplyToMostC operation</span></span>

<span data-ttu-id="85c12-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="85c12-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="85c12-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85c12-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85c12-105">Wendet einen Vorgang auf alle bis auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="85c12-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="85c12-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85c12-106">Description</span></span>

<span data-ttu-id="85c12-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="85c12-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="85c12-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85c12-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="85c12-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="85c12-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="85c12-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="85c12-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="85c12-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="85c12-111">targets : 'T[]</span></span>

<span data-ttu-id="85c12-112">Ein Array von Zielen, von denen alle außer der letzten angewendet werden `op` .</span><span class="sxs-lookup"><span data-stu-id="85c12-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="85c12-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="85c12-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="85c12-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="85c12-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="85c12-115">GIF</span><span class="sxs-lookup"><span data-stu-id="85c12-115">'T</span></span>

<span data-ttu-id="85c12-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85c12-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="85c12-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85c12-117">See Also</span></span>

- [<span data-ttu-id="85c12-118">Microsoft. Quantum. Canon. applytomost</span><span class="sxs-lookup"><span data-stu-id="85c12-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="85c12-119">Microsoft. Quantum. Canon. applytomosta</span><span class="sxs-lookup"><span data-stu-id="85c12-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="85c12-120">Microsoft. Quantum. Canon. applytomostca</span><span class="sxs-lookup"><span data-stu-id="85c12-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)