---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Applydetailca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: afb9eaa277814d7434b00a5c853a0c002190c1ae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207852"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="19626-102">Applydetailca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="19626-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="19626-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="19626-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="19626-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="19626-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="19626-105">Wendet einen Vorgang auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="19626-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="19626-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19626-106">Description</span></span>

<span data-ttu-id="19626-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="19626-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="19626-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19626-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="19626-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="19626-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="19626-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="19626-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="19626-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="19626-111">targets : 'T[]</span></span>

<span data-ttu-id="19626-112">Ein Array von Zielen, auf das der letzte angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="19626-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="19626-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="19626-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="19626-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="19626-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="19626-115">GIF</span><span class="sxs-lookup"><span data-stu-id="19626-115">'T</span></span>

<span data-ttu-id="19626-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="19626-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="19626-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="19626-117">See Also</span></span>

- [<span data-ttu-id="19626-118">Microsoft. Quantum. Canon. applyumtail</span><span class="sxs-lookup"><span data-stu-id="19626-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="19626-119">Microsoft. Quantum. Canon. applyumtaila</span><span class="sxs-lookup"><span data-stu-id="19626-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="19626-120">Microsoft. Quantum. Canon. Apply| tailc</span><span class="sxs-lookup"><span data-stu-id="19626-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)