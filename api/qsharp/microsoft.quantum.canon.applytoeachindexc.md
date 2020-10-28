---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexC
title: Applydeeachindexc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexC
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 387d7ea24b9251386a71b42a1f51ce70933bf6fc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704946"
---
# <a name="applytoeachindexc-operation"></a><span data-ttu-id="683f5-102">Applydeeachindexc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="683f5-102">ApplyToEachIndexC operation</span></span>

<span data-ttu-id="683f5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="683f5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="683f5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="683f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="683f5-105">Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.</span><span class="sxs-lookup"><span data-stu-id="683f5-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="683f5-106">Der-Modifizierer `C` gibt an, dass der Single-Qubit-Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="683f5-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachIndexC<'T> (singleElementOperation : ((Int, 'T) => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="683f5-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="683f5-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-ctl"></a><span data-ttu-id="683f5-108">singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="683f5-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="683f5-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="683f5-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="683f5-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="683f5-110">register : 'T[]</span></span>

<span data-ttu-id="683f5-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="683f5-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="683f5-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="683f5-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="683f5-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="683f5-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="683f5-114">GIF</span><span class="sxs-lookup"><span data-stu-id="683f5-114">'T</span></span>

<span data-ttu-id="683f5-115">Das Ziel, für das jeder der Vorgänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="683f5-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="683f5-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="683f5-116">See Also</span></span>

- [<span data-ttu-id="683f5-117">Microsoft. Quantum. Canon. applyteachindex</span><span class="sxs-lookup"><span data-stu-id="683f5-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)