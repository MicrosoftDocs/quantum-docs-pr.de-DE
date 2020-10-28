---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: Applydeeachindexa-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 0fe0697e6f1d9441c2d2ad2c7396f6da8daa0e1e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704951"
---
# <a name="applytoeachindexa-operation"></a><span data-ttu-id="58d55-102">Applydeeachindexa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="58d55-102">ApplyToEachIndexA operation</span></span>

<span data-ttu-id="58d55-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="58d55-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="58d55-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="58d55-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="58d55-105">Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.</span><span class="sxs-lookup"><span data-stu-id="58d55-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="58d55-106">Der-Modifizierer `A` gibt an, dass der Single-Qubit-Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="58d55-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="58d55-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="58d55-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-adj"></a><span data-ttu-id="58d55-108">singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="58d55-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="58d55-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="58d55-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="58d55-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="58d55-110">register : 'T[]</span></span>

<span data-ttu-id="58d55-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58d55-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="58d55-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="58d55-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="58d55-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="58d55-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="58d55-114">GIF</span><span class="sxs-lookup"><span data-stu-id="58d55-114">'T</span></span>

<span data-ttu-id="58d55-115">Das Ziel, für das jeder der Vorgänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="58d55-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="58d55-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="58d55-116">See Also</span></span>

- [<span data-ttu-id="58d55-117">Microsoft. Quantum. Canon. applyteachindex</span><span class="sxs-lookup"><span data-stu-id="58d55-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)