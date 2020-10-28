---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Applydeeachca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: b24fbb8c7a1a55c0a7750c5d096a61f4824dadfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704959"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="b463d-102">Applydeeachca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b463d-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="b463d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b463d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b463d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b463d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b463d-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="b463d-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="b463d-106">Der-Modifizierer `CA` gibt an, dass der Single-Qubit-Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="b463d-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b463d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b463d-107">Input</span></span>

### <a name="singleelementoperation--t--unit-adj--ctl"></a><span data-ttu-id="b463d-108">singleelementoperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="b463d-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="b463d-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b463d-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="b463d-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="b463d-110">register : 'T[]</span></span>

<span data-ttu-id="b463d-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b463d-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b463d-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b463d-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b463d-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b463d-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b463d-114">GIF</span><span class="sxs-lookup"><span data-stu-id="b463d-114">'T</span></span>

<span data-ttu-id="b463d-115">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="b463d-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="b463d-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b463d-116">See Also</span></span>

- [<span data-ttu-id="b463d-117">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="b463d-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)