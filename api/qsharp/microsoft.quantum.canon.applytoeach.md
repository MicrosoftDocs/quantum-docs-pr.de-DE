---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Applydeeach-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: e1625829e2e9efd9d39fe0692f01c1cbbffc651c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704983"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="77800-102">Applydeeach-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77800-102">ApplyToEach operation</span></span>

<span data-ttu-id="77800-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="77800-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="77800-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="77800-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="77800-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="77800-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="77800-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77800-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="77800-107">singleelementoperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77800-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="77800-108">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="77800-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="77800-109">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="77800-109">register : 'T[]</span></span>

<span data-ttu-id="77800-110">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="77800-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="77800-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77800-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="77800-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="77800-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="77800-113">GIF</span><span class="sxs-lookup"><span data-stu-id="77800-113">'T</span></span>

<span data-ttu-id="77800-114">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="77800-114">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="77800-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="77800-115">See Also</span></span>

- [<span data-ttu-id="77800-116">Microsoft. Quantum. Canon. applyumeachc</span><span class="sxs-lookup"><span data-stu-id="77800-116">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="77800-117">Microsoft. Quantum. Canon. applyumeacha</span><span class="sxs-lookup"><span data-stu-id="77800-117">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="77800-118">Microsoft. Quantum. Canon. applyumeachca</span><span class="sxs-lookup"><span data-stu-id="77800-118">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)