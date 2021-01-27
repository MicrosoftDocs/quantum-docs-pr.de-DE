---
uid: Microsoft.Quantum.Canon.NoOp
title: NOOP-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 45f3c8c9d4bae8ac8f7f60c4e4f8ead5d92e7c00
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852389"
---
# <a name="noop-operation"></a><span data-ttu-id="76ab4-102">NOOP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="76ab4-102">NoOp operation</span></span>

<span data-ttu-id="76ab4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="76ab4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="76ab4-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="76ab4-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="76ab4-105">Führt den Identitäts Vorgang (No-OP) für ein Argument aus.</span><span class="sxs-lookup"><span data-stu-id="76ab4-105">Performs the identity operation (no-op) on an argument.</span></span>

```qsharp
operation NoOp<'T> (input : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="76ab4-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76ab4-106">Description</span></span>

<span data-ttu-id="76ab4-107">Bei diesem Vorgang wird ein beliebiger Typ verwendet, und es wird keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76ab4-107">This operation takes a value of any type and does nothing to it.</span></span>
<span data-ttu-id="76ab4-108">Dies kann hilfreich sein, wenn eine Eingabe eines Vorgangs Typs erwartet wird, aber keine Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76ab4-108">This can be useful whenever an input of an operation type is expected, but no action should be taken.</span></span>
<span data-ttu-id="76ab4-109">Wenn beispielsweise ein bestimmtes Fehlerkorrektur-Syndrom anzeigt, dass kein Fehler aufgetreten ist, ist `NoOp<Qubit[]>` möglicherweise die richtige Wiederherstellungs Prozedur.</span><span class="sxs-lookup"><span data-stu-id="76ab4-109">For instance, if a particular error correction syndrome indicates that no error has occurred, `NoOp<Qubit[]>` may be the correct recovery procedure.</span></span>
<span data-ttu-id="76ab4-110">Ebenso kann, wenn ein Vorgang ein Zustands Vorbereitungsverfahren erwartet, als Eingabe `NoOp<Qubit[]>` verwendet werden, um den Status $ \ket{0 \cdots 0} $ vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="76ab4-110">Similarly, if an operation expects a state preparation procedure as input, `NoOp<Qubit[]>` can be used to prepare the state $\ket{0 \cdots 0}$.</span></span>

## <a name="input"></a><span data-ttu-id="76ab4-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="76ab4-111">Input</span></span>

### <a name="input--t"></a><span data-ttu-id="76ab4-112">Eingabe: 't</span><span class="sxs-lookup"><span data-stu-id="76ab4-112">input : 'T</span></span>

<span data-ttu-id="76ab4-113">Ein Wert, der ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="76ab4-113">A value to be ignored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="76ab4-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="76ab4-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="76ab4-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="76ab4-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="76ab4-116">GIF</span><span class="sxs-lookup"><span data-stu-id="76ab4-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="76ab4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76ab4-117">Remarks</span></span>

<span data-ttu-id="76ab4-118">In fast allen Fällen muss der Typparameter für `NoOp` explizit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76ab4-118">In almost all cases, the type parameter for `NoOp` needs to be specified explicitly.</span></span> <span data-ttu-id="76ab4-119">Beispielsweise `NoOp<Qubit>` ist identisch mit <xref:microsoft.quantum.intrinsic.i> .</span><span class="sxs-lookup"><span data-stu-id="76ab4-119">For instance, `NoOp<Qubit>` is identical to <xref:microsoft.quantum.intrinsic.i>.</span></span>

## <a name="see-also"></a><span data-ttu-id="76ab4-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="76ab4-120">See Also</span></span>

- [<span data-ttu-id="76ab4-121">Microsoft. Quantum. intrinsisch. I</span><span class="sxs-lookup"><span data-stu-id="76ab4-121">Microsoft.Quantum.Intrinsic.I</span></span>](xref:Microsoft.Quantum.Intrinsic.I)