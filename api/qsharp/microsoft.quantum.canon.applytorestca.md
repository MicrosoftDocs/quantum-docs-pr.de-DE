---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Applyorestca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: e64eeaae2151a28c289e3e71e47f897d6c378b36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841242"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="7f12e-102">Applyorestca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7f12e-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="7f12e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7f12e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7f12e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7f12e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7f12e-105">Wendet einen Vorgang auf alle außer auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="7f12e-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="7f12e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f12e-106">Description</span></span>

<span data-ttu-id="7f12e-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="7f12e-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="7f12e-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7f12e-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="7f12e-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="7f12e-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7f12e-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7f12e-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="7f12e-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="7f12e-111">targets : 'T[]</span></span>

<span data-ttu-id="7f12e-112">Ein Array von Zielen, von denen alle außer der ersten übernommen werden `op` .</span><span class="sxs-lookup"><span data-stu-id="7f12e-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7f12e-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7f12e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7f12e-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7f12e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7f12e-115">GIF</span><span class="sxs-lookup"><span data-stu-id="7f12e-115">'T</span></span>

<span data-ttu-id="7f12e-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f12e-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f12e-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7f12e-117">See Also</span></span>

- [<span data-ttu-id="7f12e-118">Microsoft. Quantum. Canon. applytor EST</span><span class="sxs-lookup"><span data-stu-id="7f12e-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="7f12e-119">Microsoft. Quantum. Canon. applytoriesta</span><span class="sxs-lookup"><span data-stu-id="7f12e-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="7f12e-120">Microsoft. Quantum. Canon. applytor</span><span class="sxs-lookup"><span data-stu-id="7f12e-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)