---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Vorgang "zugswatmustncallsca"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: bb6ba2615b571b0d9d056b93f8e36d2dec0c4a21
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853533"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="5f762-102">Vorgang "zugswatmustncallsca"</span><span class="sxs-lookup"><span data-stu-id="5f762-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="5f762-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="5f762-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="5f762-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5f762-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5f762-105">Bei einem Aufruf dieses Vorgangs und seines Adjoint-Vorgangs bestätigt, dass ein angegebener Vorgang höchstens eine bestimmte Anzahl von Vorkommen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5f762-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="5f762-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f762-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="5f762-107">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5f762-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5f762-108">Die maximale Anzahl von aufrufen, die `op` aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="5f762-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput--is-adj--ctl"></a><span data-ttu-id="5f762-109">OP: ' TInput => ' TOutput ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="5f762-109">op : 'TInput => 'TOutput  is Adj + Ctl</span></span>

<span data-ttu-id="5f762-110">Ein Vorgang, dessen Aufrufe eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="5f762-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="5f762-111">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="5f762-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="5f762-112">Eine Meldung, die bei einem Fehler angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f762-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5f762-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5f762-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5f762-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="5f762-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="5f762-115">' TInput</span><span class="sxs-lookup"><span data-stu-id="5f762-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="5f762-116">"TOutput"</span><span class="sxs-lookup"><span data-stu-id="5f762-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="5f762-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5f762-117">Example</span></span>

<span data-ttu-id="5f762-118">Der folgende Code Ausschnitt schlägt fehl, wenn er auf Computern ausgeführt wird, die diese Diagnose unterstützen:</span><span class="sxs-lookup"><span data-stu-id="5f762-118">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
using (register = Qubit[4]) {
    within {
        AllowAtMostNCallsCA(3, H, "Too many calls to H.");
    } apply {
        // Fails since this calls H four times, rather than the
        // allowed maximum of three.
        ApplyToEach(H, register);
    }
}
```

## <a name="remarks"></a><span data-ttu-id="5f762-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f762-119">Remarks</span></span>

<span data-ttu-id="5f762-120">Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5f762-120">This operation may be replaced by a no-op on targets which do not support it.</span></span>