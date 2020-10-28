---
uid: Microsoft.Quantum.Canon.NoOp
title: NOOP-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 987e39577c3b736418234431ed7a915ae461f763
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703949"
---
# <a name="noop-operation"></a><span data-ttu-id="d4e92-102">NOOP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d4e92-102">NoOp operation</span></span>

<span data-ttu-id="d4e92-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d4e92-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d4e92-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d4e92-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d4e92-105">Führt den Identitäts Vorgang (No-OP) für ein Argument aus.</span><span class="sxs-lookup"><span data-stu-id="d4e92-105">Performs the identity operation (no-op) on an argument.</span></span>

```qsharp
operation NoOp<'T> (input : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="d4e92-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4e92-106">Description</span></span>

<span data-ttu-id="d4e92-107">Bei diesem Vorgang wird ein beliebiger Typ verwendet, und es wird keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4e92-107">This operation takes a value of any type and does nothing to it.</span></span>
<span data-ttu-id="d4e92-108">Dies kann hilfreich sein, wenn eine Eingabe eines Vorgangs Typs erwartet wird, aber keine Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4e92-108">This can be useful whenever an input of an operation type is expected, but no action should be taken.</span></span>
<span data-ttu-id="d4e92-109">Wenn beispielsweise ein bestimmtes Fehlerkorrektur-Syndrom anzeigt, dass kein Fehler aufgetreten ist, ist `NoOp<Qubit[]>` möglicherweise die richtige Wiederherstellungs Prozedur.</span><span class="sxs-lookup"><span data-stu-id="d4e92-109">For instance, if a particular error correction syndrome indicates that no error has occurred, `NoOp<Qubit[]>` may be the correct recovery procedure.</span></span>
<span data-ttu-id="d4e92-110">Ebenso kann, wenn ein Vorgang ein Zustands Vorbereitungsverfahren erwartet, als Eingabe `NoOp<Qubit[]>` verwendet werden, um den Status $ \ket{0 \cdots 0} $ vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="d4e92-110">Similarly, if an operation expects a state preparation procedure as input, `NoOp<Qubit[]>` can be used to prepare the state $\ket{0 \cdots 0}$.</span></span>

## <a name="input"></a><span data-ttu-id="d4e92-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4e92-111">Input</span></span>

### <a name="input--t"></a><span data-ttu-id="d4e92-112">Eingabe: 't</span><span class="sxs-lookup"><span data-stu-id="d4e92-112">input : 'T</span></span>

<span data-ttu-id="d4e92-113">Ein Wert, der ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4e92-113">A value to be ignored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d4e92-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4e92-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d4e92-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d4e92-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d4e92-116">GIF</span><span class="sxs-lookup"><span data-stu-id="d4e92-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="d4e92-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d4e92-117">Remarks</span></span>

<span data-ttu-id="d4e92-118">In fast allen Fällen muss der Typparameter für `NoOp` explizit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d4e92-118">In almost all cases, the type parameter for `NoOp` needs to be specified explicitly.</span></span> <span data-ttu-id="d4e92-119">Beispielsweise `NoOp<Qubit>` ist identisch mit <xref:microsoft.quantum.intrinsic.i> .</span><span class="sxs-lookup"><span data-stu-id="d4e92-119">For instance, `NoOp<Qubit>` is identical to <xref:microsoft.quantum.intrinsic.i>.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4e92-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4e92-120">See Also</span></span>

- [<span data-ttu-id="d4e92-121">Microsoft. Quantum. intrinsisch. I</span><span class="sxs-lookup"><span data-stu-id="d4e92-121">Microsoft.Quantum.Intrinsic.I</span></span>](xref:Microsoft.Quantum.Intrinsic.I)