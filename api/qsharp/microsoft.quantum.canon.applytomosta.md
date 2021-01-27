---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Applytomosta-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: eb793b3d6bc1f75a14e97420d36d0aea3038e0f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850575"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="7ae91-102">Applytomosta-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7ae91-102">ApplyToMostA operation</span></span>

<span data-ttu-id="7ae91-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7ae91-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7ae91-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7ae91-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7ae91-105">Wendet einen Vorgang auf alle bis auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="7ae91-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="7ae91-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ae91-106">Description</span></span>

<span data-ttu-id="7ae91-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="7ae91-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="7ae91-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ae91-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="7ae91-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="7ae91-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="7ae91-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7ae91-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="7ae91-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="7ae91-111">targets : 'T[]</span></span>

<span data-ttu-id="7ae91-112">Ein Array von Zielen, von denen alle außer der letzten angewendet werden `op` .</span><span class="sxs-lookup"><span data-stu-id="7ae91-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7ae91-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7ae91-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7ae91-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7ae91-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7ae91-115">GIF</span><span class="sxs-lookup"><span data-stu-id="7ae91-115">'T</span></span>

<span data-ttu-id="7ae91-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ae91-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ae91-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7ae91-117">See Also</span></span>

- [<span data-ttu-id="7ae91-118">Microsoft. Quantum. Canon. applytomost</span><span class="sxs-lookup"><span data-stu-id="7ae91-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="7ae91-119">Microsoft. Quantum. Canon. applytomostc</span><span class="sxs-lookup"><span data-stu-id="7ae91-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="7ae91-120">Microsoft. Quantum. Canon. applytomostca</span><span class="sxs-lookup"><span data-stu-id="7ae91-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)