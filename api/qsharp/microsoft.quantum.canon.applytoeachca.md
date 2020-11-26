---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Applydeeachca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: dcfd4619a77413e71044e6a7d5fc19a9f22bbf94
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217746"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="73b83-102">Applydeeachca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="73b83-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="73b83-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="73b83-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="73b83-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="73b83-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="73b83-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="73b83-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="73b83-106">Der-Modifizierer `CA` gibt an, dass der Single-Qubit-Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="73b83-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="73b83-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="73b83-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a><span data-ttu-id="73b83-108">singleelementoperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="73b83-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="73b83-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="73b83-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="73b83-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="73b83-110">register : 'T[]</span></span>

<span data-ttu-id="73b83-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="73b83-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="73b83-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="73b83-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="73b83-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="73b83-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="73b83-114">GIF</span><span class="sxs-lookup"><span data-stu-id="73b83-114">'T</span></span>

<span data-ttu-id="73b83-115">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="73b83-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="73b83-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="73b83-116">See Also</span></span>

- [<span data-ttu-id="73b83-117">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="73b83-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)