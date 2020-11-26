---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Applytoriesta-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 34cb5071dd939d0831e39bb8f1670670ae1fad31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208300"
---
# <a name="applytoresta-operation"></a><span data-ttu-id="98a50-102">Applytoriesta-Vorgang</span><span class="sxs-lookup"><span data-stu-id="98a50-102">ApplyToRestA operation</span></span>

<span data-ttu-id="98a50-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="98a50-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="98a50-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="98a50-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="98a50-105">Wendet einen Vorgang auf alle außer auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="98a50-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="98a50-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98a50-106">Description</span></span>

<span data-ttu-id="98a50-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="98a50-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="98a50-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="98a50-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="98a50-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="98a50-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="98a50-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="98a50-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="98a50-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="98a50-111">targets : 'T[]</span></span>

<span data-ttu-id="98a50-112">Ein Array von Zielen, von denen alle außer der ersten übernommen werden `op` .</span><span class="sxs-lookup"><span data-stu-id="98a50-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="98a50-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="98a50-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="98a50-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="98a50-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="98a50-115">GIF</span><span class="sxs-lookup"><span data-stu-id="98a50-115">'T</span></span>

<span data-ttu-id="98a50-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98a50-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="98a50-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98a50-117">See Also</span></span>

- [<span data-ttu-id="98a50-118">Microsoft. Quantum. Canon. applytor EST</span><span class="sxs-lookup"><span data-stu-id="98a50-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="98a50-119">Microsoft. Quantum. Canon. applytor</span><span class="sxs-lookup"><span data-stu-id="98a50-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="98a50-120">Microsoft. Quantum. Canon. applytor estca</span><span class="sxs-lookup"><span data-stu-id="98a50-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)