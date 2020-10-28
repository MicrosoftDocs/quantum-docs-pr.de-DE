---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Vorgang "zugswatmustncallsca"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 1a9975d2d2026749238430b247cf47738de545cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702792"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="bb99f-102">Vorgang "zugswatmustncallsca"</span><span class="sxs-lookup"><span data-stu-id="bb99f-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="bb99f-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="bb99f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="bb99f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bb99f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bb99f-105">Bei einem Aufruf dieses Vorgangs und seines Adjoint-Vorgangs bestätigt, dass ein angegebener Vorgang höchstens eine bestimmte Anzahl von Vorkommen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bb99f-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="bb99f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bb99f-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="bb99f-107">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bb99f-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bb99f-108">Die maximale Anzahl von aufrufen, die `op` aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="bb99f-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput-adj--ctl"></a><span data-ttu-id="bb99f-109">OP: ' TInput => ' TOutput ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="bb99f-109">op : 'TInput => 'TOutput Adj + Ctl</span></span>

<span data-ttu-id="bb99f-110">Ein Vorgang, dessen Aufrufe eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="bb99f-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="bb99f-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="bb99f-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="bb99f-112">Eine Meldung, die bei einem Fehler angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb99f-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bb99f-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bb99f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bb99f-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="bb99f-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="bb99f-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="bb99f-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="bb99f-116">"TOutput"</span><span class="sxs-lookup"><span data-stu-id="bb99f-116">'TOutput</span></span>



## <a name="remarks"></a><span data-ttu-id="bb99f-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb99f-117">Remarks</span></span>

<span data-ttu-id="bb99f-118">Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bb99f-118">This operation may be replaced by a no-op on targets which do not support it.</span></span>