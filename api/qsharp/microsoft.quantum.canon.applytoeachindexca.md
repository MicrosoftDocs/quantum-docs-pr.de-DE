---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Applydeeachindexca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: c5bb61aadbdaab9c74a3dcd418088c532b495ff5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704938"
---
# <a name="applytoeachindexca-operation"></a><span data-ttu-id="d35e6-102">Applydeeachindexca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d35e6-102">ApplyToEachIndexCA operation</span></span>

<span data-ttu-id="d35e6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d35e6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d35e6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d35e6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d35e6-105">Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.</span><span class="sxs-lookup"><span data-stu-id="d35e6-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="d35e6-106">Der-Modifizierer `CA` gibt an, dass der Single-Qubit-Vorgang adjointable und steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="d35e6-106">The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.</span></span>

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d35e6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d35e6-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-adj--ctl"></a><span data-ttu-id="d35e6-108">singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="d35e6-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="d35e6-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d35e6-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="d35e6-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="d35e6-110">register : 'T[]</span></span>

<span data-ttu-id="d35e6-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d35e6-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d35e6-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d35e6-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d35e6-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d35e6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d35e6-114">GIF</span><span class="sxs-lookup"><span data-stu-id="d35e6-114">'T</span></span>

<span data-ttu-id="d35e6-115">Das Ziel, für das jeder der Vorgänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="d35e6-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="d35e6-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d35e6-116">See Also</span></span>

- [<span data-ttu-id="d35e6-117">Microsoft. Quantum. Canon. applyteachindex</span><span class="sxs-lookup"><span data-stu-id="d35e6-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)