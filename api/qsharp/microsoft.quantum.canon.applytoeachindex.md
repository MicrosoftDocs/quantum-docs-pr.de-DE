---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Applydeeachindex-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 4ce184b34add9238e26f9b35b40ec0bddb23ccf9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704954"
---
# <a name="applytoeachindex-operation"></a><span data-ttu-id="34d3e-102">Applydeeachindex-Vorgang</span><span class="sxs-lookup"><span data-stu-id="34d3e-102">ApplyToEachIndex operation</span></span>

<span data-ttu-id="34d3e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="34d3e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="34d3e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="34d3e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="34d3e-105">Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.</span><span class="sxs-lookup"><span data-stu-id="34d3e-105">Applies a single-qubit operation to each indexed element in a register.</span></span>

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="34d3e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34d3e-106">Input</span></span>

### <a name="singleelementoperation--intt--unit"></a><span data-ttu-id="34d3e-107">singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="34d3e-107">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="34d3e-108">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="34d3e-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="34d3e-109">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="34d3e-109">register : 'T[]</span></span>

<span data-ttu-id="34d3e-110">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="34d3e-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="34d3e-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="34d3e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="34d3e-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="34d3e-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="34d3e-113">GIF</span><span class="sxs-lookup"><span data-stu-id="34d3e-113">'T</span></span>

<span data-ttu-id="34d3e-114">Das Ziel, für das jeder der Vorgänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="34d3e-114">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="34d3e-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="34d3e-115">See Also</span></span>

- [<span data-ttu-id="34d3e-116">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="34d3e-116">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [<span data-ttu-id="34d3e-117">Microsoft. Quantum. Canon. applyteachindexa</span><span class="sxs-lookup"><span data-stu-id="34d3e-117">Microsoft.Quantum.Canon.ApplyToEachIndexA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [<span data-ttu-id="34d3e-118">Microsoft. Quantum. Canon. applyteachindexc</span><span class="sxs-lookup"><span data-stu-id="34d3e-118">Microsoft.Quantum.Canon.ApplyToEachIndexC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [<span data-ttu-id="34d3e-119">Microsoft. Quantum. Canon. applyteachindexca</span><span class="sxs-lookup"><span data-stu-id="34d3e-119">Microsoft.Quantum.Canon.ApplyToEachIndexCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)