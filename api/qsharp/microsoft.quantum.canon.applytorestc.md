---
uid: Microsoft.Quantum.Canon.ApplyToRestC
title: Applytor-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestC
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 1e533a9f0994b70054aeca2f9ddd97f4e200b03f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850496"
---
# <a name="applytorestc-operation"></a><span data-ttu-id="11953-102">Applytor-Vorgang</span><span class="sxs-lookup"><span data-stu-id="11953-102">ApplyToRestC operation</span></span>

<span data-ttu-id="11953-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="11953-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="11953-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11953-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11953-105">Wendet einen Vorgang auf alle außer auf das erste Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="11953-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="11953-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11953-106">Description</span></span>

<span data-ttu-id="11953-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="11953-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="11953-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="11953-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="11953-109">OP: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="11953-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="11953-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="11953-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="11953-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="11953-111">targets : 'T[]</span></span>

<span data-ttu-id="11953-112">Ein Array von Zielen, von denen alle außer der ersten übernommen werden `op` .</span><span class="sxs-lookup"><span data-stu-id="11953-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="11953-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="11953-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="11953-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="11953-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="11953-115">GIF</span><span class="sxs-lookup"><span data-stu-id="11953-115">'T</span></span>

<span data-ttu-id="11953-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11953-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="11953-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="11953-117">See Also</span></span>

- [<span data-ttu-id="11953-118">Microsoft. Quantum. Canon. applytor EST</span><span class="sxs-lookup"><span data-stu-id="11953-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="11953-119">Microsoft. Quantum. Canon. applytoriesta</span><span class="sxs-lookup"><span data-stu-id="11953-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="11953-120">Microsoft. Quantum. Canon. applytor estca</span><span class="sxs-lookup"><span data-stu-id="11953-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)