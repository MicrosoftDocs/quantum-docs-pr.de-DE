---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: Applydeeachindexa-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: fb278f217ac450ab48aa37b0035cd1bdd295d3e5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850824"
---
# <a name="applytoeachindexa-operation"></a><span data-ttu-id="f6d52-102">Applydeeachindexa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f6d52-102">ApplyToEachIndexA operation</span></span>

<span data-ttu-id="f6d52-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f6d52-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f6d52-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f6d52-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f6d52-105">Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.</span><span class="sxs-lookup"><span data-stu-id="f6d52-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="f6d52-106">Der-Modifizierer `A` gibt an, dass der Single-Qubit-Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="f6d52-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="f6d52-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6d52-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj"></a><span data-ttu-id="f6d52-108">singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="f6d52-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="f6d52-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f6d52-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="f6d52-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="f6d52-110">register : 'T[]</span></span>

<span data-ttu-id="f6d52-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6d52-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f6d52-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f6d52-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f6d52-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f6d52-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f6d52-114">GIF</span><span class="sxs-lookup"><span data-stu-id="f6d52-114">'T</span></span>

<span data-ttu-id="f6d52-115">Das Ziel, für das jeder der Vorgänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="f6d52-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6d52-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f6d52-116">See Also</span></span>

- [<span data-ttu-id="f6d52-117">Microsoft. Quantum. Canon. applyteachindex</span><span class="sxs-lookup"><span data-stu-id="f6d52-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)