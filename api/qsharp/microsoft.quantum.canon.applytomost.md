---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: Applytomost-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a3918233e101f3d8956601dcc7d85edcf6196ac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850587"
---
# <a name="applytomost-operation"></a><span data-ttu-id="25218-102">Applytomost-Vorgang</span><span class="sxs-lookup"><span data-stu-id="25218-102">ApplyToMost operation</span></span>

<span data-ttu-id="25218-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="25218-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="25218-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25218-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25218-105">Wendet einen Vorgang auf alle bis auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="25218-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="25218-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25218-106">Description</span></span>

<span data-ttu-id="25218-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="25218-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="25218-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25218-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="25218-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="25218-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="25218-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="25218-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="25218-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="25218-111">targets : 'T[]</span></span>

<span data-ttu-id="25218-112">Ein Array von Zielen, von denen alle außer der letzten angewendet werden `op` .</span><span class="sxs-lookup"><span data-stu-id="25218-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="25218-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="25218-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="25218-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="25218-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="25218-115">GIF</span><span class="sxs-lookup"><span data-stu-id="25218-115">'T</span></span>

<span data-ttu-id="25218-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="25218-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="25218-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="25218-117">Example</span></span>

<span data-ttu-id="25218-118">Die folgenden Q #-Code Ausschnitte sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="25218-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToMost(ApplyCNOTChain, register);
ApplyCNOTChain(Most(register));
```

## <a name="see-also"></a><span data-ttu-id="25218-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="25218-119">See Also</span></span>

- [<span data-ttu-id="25218-120">Microsoft. Quantum. Canon. applytomosta</span><span class="sxs-lookup"><span data-stu-id="25218-120">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="25218-121">Microsoft. Quantum. Canon. applytomostc</span><span class="sxs-lookup"><span data-stu-id="25218-121">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="25218-122">Microsoft. Quantum. Canon. applytomostca</span><span class="sxs-lookup"><span data-stu-id="25218-122">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)