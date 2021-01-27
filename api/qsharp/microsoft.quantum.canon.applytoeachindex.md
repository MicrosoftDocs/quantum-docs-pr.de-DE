---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Applydeeachindex-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 8b34dc24580a3df7ae2c13ef87a6fa10c7afd3f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844591"
---
# <a name="applytoeachindex-operation"></a><span data-ttu-id="8e91f-102">Applydeeachindex-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8e91f-102">ApplyToEachIndex operation</span></span>

<span data-ttu-id="8e91f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8e91f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8e91f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e91f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e91f-105">Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.</span><span class="sxs-lookup"><span data-stu-id="8e91f-105">Applies a single-qubit operation to each indexed element in a register.</span></span>

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="8e91f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e91f-106">Input</span></span>

### <a name="singleelementoperation--intt--unit"></a><span data-ttu-id="8e91f-107">singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8e91f-107">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8e91f-108">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8e91f-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="8e91f-109">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="8e91f-109">register : 'T[]</span></span>

<span data-ttu-id="8e91f-110">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e91f-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8e91f-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8e91f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8e91f-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="8e91f-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8e91f-113">GIF</span><span class="sxs-lookup"><span data-stu-id="8e91f-113">'T</span></span>

<span data-ttu-id="8e91f-114">Das Ziel, für das jeder der Vorgänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="8e91f-114">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e91f-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e91f-115">See Also</span></span>

- [<span data-ttu-id="8e91f-116">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="8e91f-116">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [<span data-ttu-id="8e91f-117">Microsoft. Quantum. Canon. applyteachindexa</span><span class="sxs-lookup"><span data-stu-id="8e91f-117">Microsoft.Quantum.Canon.ApplyToEachIndexA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [<span data-ttu-id="8e91f-118">Microsoft. Quantum. Canon. applyteachindexc</span><span class="sxs-lookup"><span data-stu-id="8e91f-118">Microsoft.Quantum.Canon.ApplyToEachIndexC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [<span data-ttu-id="8e91f-119">Microsoft. Quantum. Canon. applyteachindexca</span><span class="sxs-lookup"><span data-stu-id="8e91f-119">Microsoft.Quantum.Canon.ApplyToEachIndexCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)