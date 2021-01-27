---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Applydeeachindexca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: 5046edc54576420bd8919ca52947076aed17cbce
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850798"
---
# <a name="applytoeachindexca-operation"></a><span data-ttu-id="59b04-102">Applydeeachindexca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="59b04-102">ApplyToEachIndexCA operation</span></span>

<span data-ttu-id="59b04-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="59b04-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="59b04-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="59b04-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="59b04-105">Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.</span><span class="sxs-lookup"><span data-stu-id="59b04-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="59b04-106">Der-Modifizierer `CA` gibt an, dass der Single-Qubit-Vorgang adjointable und steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="59b04-106">The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.</span></span>

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="59b04-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59b04-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj--ctl"></a><span data-ttu-id="59b04-108">singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="59b04-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="59b04-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="59b04-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="59b04-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="59b04-110">register : 'T[]</span></span>

<span data-ttu-id="59b04-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="59b04-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="59b04-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="59b04-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="59b04-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="59b04-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="59b04-114">GIF</span><span class="sxs-lookup"><span data-stu-id="59b04-114">'T</span></span>

<span data-ttu-id="59b04-115">Das Ziel, für das jeder der Vorgänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="59b04-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="59b04-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="59b04-116">See Also</span></span>

- [<span data-ttu-id="59b04-117">Microsoft. Quantum. Canon. applyteachindex</span><span class="sxs-lookup"><span data-stu-id="59b04-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)