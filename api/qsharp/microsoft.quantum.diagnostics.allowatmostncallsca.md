---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Vorgang "zugswatmustncallsca"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 7caf33e33318bb74cb160436940eff9f0f2782cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202565"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="10c1e-102">Vorgang "zugswatmustncallsca"</span><span class="sxs-lookup"><span data-stu-id="10c1e-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="10c1e-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="10c1e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="10c1e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="10c1e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="10c1e-105">Bei einem Aufruf dieses Vorgangs und seines Adjoint-Vorgangs bestätigt, dass ein angegebener Vorgang höchstens eine bestimmte Anzahl von Vorkommen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="10c1e-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="10c1e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="10c1e-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="10c1e-107">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="10c1e-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="10c1e-108">Die maximale Anzahl von aufrufen, die `op` aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="10c1e-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput--is-adj--ctl"></a><span data-ttu-id="10c1e-109">OP: ' TInput => ' TOutput ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="10c1e-109">op : 'TInput => 'TOutput  is Adj + Ctl</span></span>

<span data-ttu-id="10c1e-110">Ein Vorgang, dessen Aufrufe eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="10c1e-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="10c1e-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="10c1e-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="10c1e-112">Eine Meldung, die bei einem Fehler angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10c1e-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="10c1e-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="10c1e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="10c1e-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="10c1e-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="10c1e-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="10c1e-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="10c1e-116">"TOutput"</span><span class="sxs-lookup"><span data-stu-id="10c1e-116">'TOutput</span></span>



## <a name="remarks"></a><span data-ttu-id="10c1e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10c1e-117">Remarks</span></span>

<span data-ttu-id="10c1e-118">Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="10c1e-118">This operation may be replaced by a no-op on targets which do not support it.</span></span>