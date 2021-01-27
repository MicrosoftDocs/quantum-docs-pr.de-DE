---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Applydeeach-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 61dda69751989ef8a98fa8fb01d832014ec4ad35
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844622"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="1551d-102">Applydeeach-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1551d-102">ApplyToEach operation</span></span>

<span data-ttu-id="1551d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1551d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1551d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1551d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1551d-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="1551d-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="1551d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1551d-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="1551d-107">singleelementoperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1551d-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1551d-108">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1551d-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="1551d-109">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="1551d-109">register : 'T[]</span></span>

<span data-ttu-id="1551d-110">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1551d-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1551d-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1551d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1551d-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1551d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1551d-113">GIF</span><span class="sxs-lookup"><span data-stu-id="1551d-113">'T</span></span>

<span data-ttu-id="1551d-114">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="1551d-114">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="1551d-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1551d-115">Example</span></span>

<span data-ttu-id="1551d-116">Bereiten Sie einen "3-Qubit $ \ket{+} $"-Status vor:</span><span class="sxs-lookup"><span data-stu-id="1551d-116">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="1551d-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1551d-117">See Also</span></span>

- [<span data-ttu-id="1551d-118">Microsoft. Quantum. Canon. applyumeachc</span><span class="sxs-lookup"><span data-stu-id="1551d-118">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="1551d-119">Microsoft. Quantum. Canon. applyumeacha</span><span class="sxs-lookup"><span data-stu-id="1551d-119">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="1551d-120">Microsoft. Quantum. Canon. applyumeachca</span><span class="sxs-lookup"><span data-stu-id="1551d-120">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)