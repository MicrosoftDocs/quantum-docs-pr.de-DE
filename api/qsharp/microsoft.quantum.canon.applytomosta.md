---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Applytomosta-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 7c226de9b2c99d124c467175dfe65a60a89d4332
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208498"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="9d676-102">Applytomosta-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9d676-102">ApplyToMostA operation</span></span>

<span data-ttu-id="9d676-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9d676-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9d676-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9d676-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9d676-105">Wendet einen Vorgang auf alle bis auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="9d676-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="9d676-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d676-106">Description</span></span>

<span data-ttu-id="9d676-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="9d676-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="9d676-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9d676-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="9d676-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="9d676-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="9d676-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9d676-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="9d676-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="9d676-111">targets : 'T[]</span></span>

<span data-ttu-id="9d676-112">Ein Array von Zielen, von denen alle außer der letzten angewendet werden `op` .</span><span class="sxs-lookup"><span data-stu-id="9d676-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9d676-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9d676-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9d676-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9d676-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9d676-115">GIF</span><span class="sxs-lookup"><span data-stu-id="9d676-115">'T</span></span>

<span data-ttu-id="9d676-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d676-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d676-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9d676-117">See Also</span></span>

- [<span data-ttu-id="9d676-118">Microsoft. Quantum. Canon. applytomost</span><span class="sxs-lookup"><span data-stu-id="9d676-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="9d676-119">Microsoft. Quantum. Canon. applytomostc</span><span class="sxs-lookup"><span data-stu-id="9d676-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="9d676-120">Microsoft. Quantum. Canon. applytomostca</span><span class="sxs-lookup"><span data-stu-id="9d676-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)