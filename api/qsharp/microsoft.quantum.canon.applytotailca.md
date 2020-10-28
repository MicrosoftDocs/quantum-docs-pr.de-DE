---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Applydetailca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 00755df80981a09ddfd8327ee9b35761d30af4f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704610"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="a29fa-102">Applydetailca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a29fa-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="a29fa-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a29fa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a29fa-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a29fa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a29fa-105">Wendet einen Vorgang auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="a29fa-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="a29fa-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a29fa-106">Description</span></span>

<span data-ttu-id="a29fa-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="a29fa-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="a29fa-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a29fa-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="a29fa-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="a29fa-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="a29fa-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a29fa-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="a29fa-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="a29fa-111">targets : 'T[]</span></span>

<span data-ttu-id="a29fa-112">Ein Array von Zielen, auf das der letzte angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="a29fa-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a29fa-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a29fa-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a29fa-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a29fa-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a29fa-115">GIF</span><span class="sxs-lookup"><span data-stu-id="a29fa-115">'T</span></span>

<span data-ttu-id="a29fa-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a29fa-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a29fa-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a29fa-117">See Also</span></span>

- [<span data-ttu-id="a29fa-118">Microsoft. Quantum. Canon. applyumtail</span><span class="sxs-lookup"><span data-stu-id="a29fa-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="a29fa-119">Microsoft. Quantum. Canon. applyumtaila</span><span class="sxs-lookup"><span data-stu-id="a29fa-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="a29fa-120">Microsoft. Quantum. Canon. Apply| tailc</span><span class="sxs-lookup"><span data-stu-id="a29fa-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)