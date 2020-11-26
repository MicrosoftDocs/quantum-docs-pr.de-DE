---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Applydeeachindex-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 746bc19f7a137ef476a25abdabc4737ed6727ff2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217611"
---
# <a name="applytoeachindex-operation"></a><span data-ttu-id="8e24b-102">Applydeeachindex-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8e24b-102">ApplyToEachIndex operation</span></span>

<span data-ttu-id="8e24b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8e24b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8e24b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e24b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e24b-105">Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.</span><span class="sxs-lookup"><span data-stu-id="8e24b-105">Applies a single-qubit operation to each indexed element in a register.</span></span>

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="8e24b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e24b-106">Input</span></span>

### <a name="singleelementoperation--intt--unit"></a><span data-ttu-id="8e24b-107">singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8e24b-107">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8e24b-108">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8e24b-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="8e24b-109">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="8e24b-109">register : 'T[]</span></span>

<span data-ttu-id="8e24b-110">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e24b-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8e24b-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8e24b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8e24b-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8e24b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8e24b-113">GIF</span><span class="sxs-lookup"><span data-stu-id="8e24b-113">'T</span></span>

<span data-ttu-id="8e24b-114">Das Ziel, für das jeder der Vorgänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="8e24b-114">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e24b-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e24b-115">See Also</span></span>

- [<span data-ttu-id="8e24b-116">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="8e24b-116">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [<span data-ttu-id="8e24b-117">Microsoft. Quantum. Canon. applyteachindexa</span><span class="sxs-lookup"><span data-stu-id="8e24b-117">Microsoft.Quantum.Canon.ApplyToEachIndexA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [<span data-ttu-id="8e24b-118">Microsoft. Quantum. Canon. applyteachindexc</span><span class="sxs-lookup"><span data-stu-id="8e24b-118">Microsoft.Quantum.Canon.ApplyToEachIndexC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [<span data-ttu-id="8e24b-119">Microsoft. Quantum. Canon. applyteachindexca</span><span class="sxs-lookup"><span data-stu-id="8e24b-119">Microsoft.Quantum.Canon.ApplyToEachIndexCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)