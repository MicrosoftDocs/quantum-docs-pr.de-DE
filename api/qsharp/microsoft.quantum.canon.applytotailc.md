---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Applydetailc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 5a68cae3fd122416cfd064e0078e03f5c00ab492
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217287"
---
# <a name="applytotailc-operation"></a><span data-ttu-id="ea80c-102">Applydetailc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ea80c-102">ApplyToTailC operation</span></span>

<span data-ttu-id="ea80c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ea80c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ea80c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ea80c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ea80c-105">Wendet einen Vorgang auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="ea80c-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="ea80c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea80c-106">Description</span></span>

<span data-ttu-id="ea80c-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ea80c-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ea80c-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ea80c-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="ea80c-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="ea80c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="ea80c-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ea80c-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ea80c-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="ea80c-111">targets : 'T[]</span></span>

<span data-ttu-id="ea80c-112">Ein Array von Zielen, auf das der letzte angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="ea80c-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ea80c-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ea80c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ea80c-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ea80c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ea80c-115">GIF</span><span class="sxs-lookup"><span data-stu-id="ea80c-115">'T</span></span>

<span data-ttu-id="ea80c-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea80c-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea80c-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ea80c-117">See Also</span></span>

- [<span data-ttu-id="ea80c-118">Microsoft. Quantum. Canon. applyumtail</span><span class="sxs-lookup"><span data-stu-id="ea80c-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="ea80c-119">Microsoft. Quantum. Canon. applyumtaila</span><span class="sxs-lookup"><span data-stu-id="ea80c-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="ea80c-120">Microsoft. Quantum. Canon. applyumtailca</span><span class="sxs-lookup"><span data-stu-id="ea80c-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)