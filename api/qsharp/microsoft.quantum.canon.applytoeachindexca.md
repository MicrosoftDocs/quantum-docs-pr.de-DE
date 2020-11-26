---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Applydeeachindexca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: abb616498a8ff9c3348df81cf0ca1a1669561eec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208940"
---
# <a name="applytoeachindexca-operation"></a><span data-ttu-id="eec88-102">Applydeeachindexca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eec88-102">ApplyToEachIndexCA operation</span></span>

<span data-ttu-id="eec88-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="eec88-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="eec88-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eec88-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eec88-105">Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.</span><span class="sxs-lookup"><span data-stu-id="eec88-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="eec88-106">Der-Modifizierer `CA` gibt an, dass der Single-Qubit-Vorgang adjointable und steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="eec88-106">The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.</span></span>

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="eec88-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="eec88-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj--ctl"></a><span data-ttu-id="eec88-108">singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="eec88-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="eec88-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="eec88-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="eec88-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="eec88-110">register : 'T[]</span></span>

<span data-ttu-id="eec88-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eec88-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eec88-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eec88-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="eec88-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="eec88-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="eec88-114">GIF</span><span class="sxs-lookup"><span data-stu-id="eec88-114">'T</span></span>

<span data-ttu-id="eec88-115">Das Ziel, für das jeder der Vorgänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="eec88-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="eec88-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eec88-116">See Also</span></span>

- [<span data-ttu-id="eec88-117">Microsoft. Quantum. Canon. applyteachindex</span><span class="sxs-lookup"><span data-stu-id="eec88-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)