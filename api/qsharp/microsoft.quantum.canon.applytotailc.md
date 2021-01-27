---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Applydetailc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 8408dff24c5c57efbedb649ac182fac49e836a3e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850418"
---
# <a name="applytotailc-operation"></a><span data-ttu-id="7c5b5-102">Applydetailc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7c5b5-102">ApplyToTailC operation</span></span>

<span data-ttu-id="7c5b5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7c5b5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7c5b5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7c5b5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7c5b5-105">Wendet einen Vorgang auf das letzte Element eines Arrays an.</span><span class="sxs-lookup"><span data-stu-id="7c5b5-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="7c5b5-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c5b5-106">Description</span></span>

<span data-ttu-id="7c5b5-107">Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="7c5b5-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="7c5b5-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7c5b5-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="7c5b5-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="7c5b5-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="7c5b5-110">Ein anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7c5b5-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="7c5b5-111">Ziele: 't []</span><span class="sxs-lookup"><span data-stu-id="7c5b5-111">targets : 'T[]</span></span>

<span data-ttu-id="7c5b5-112">Ein Array von Zielen, auf das der letzte angewendet wird `op` .</span><span class="sxs-lookup"><span data-stu-id="7c5b5-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7c5b5-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7c5b5-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7c5b5-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7c5b5-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7c5b5-115">GIF</span><span class="sxs-lookup"><span data-stu-id="7c5b5-115">'T</span></span>

<span data-ttu-id="7c5b5-116">Der Eingabetyp des Vorgangs, der angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c5b5-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c5b5-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7c5b5-117">See Also</span></span>

- [<span data-ttu-id="7c5b5-118">Microsoft. Quantum. Canon. applyumtail</span><span class="sxs-lookup"><span data-stu-id="7c5b5-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="7c5b5-119">Microsoft. Quantum. Canon. applyumtaila</span><span class="sxs-lookup"><span data-stu-id="7c5b5-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="7c5b5-120">Microsoft. Quantum. Canon. applyumtailca</span><span class="sxs-lookup"><span data-stu-id="7c5b5-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)