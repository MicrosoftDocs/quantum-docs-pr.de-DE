---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Applydeeach-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 11f9363feb38676df3f805496c74036aa96160c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217865"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="fe4e1-102">Applydeeach-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fe4e1-102">ApplyToEach operation</span></span>

<span data-ttu-id="fe4e1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fe4e1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fe4e1-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fe4e1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fe4e1-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="fe4e1-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="fe4e1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe4e1-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="fe4e1-107">singleelementoperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fe4e1-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="fe4e1-108">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fe4e1-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="fe4e1-109">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="fe4e1-109">register : 'T[]</span></span>

<span data-ttu-id="fe4e1-110">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe4e1-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fe4e1-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fe4e1-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="fe4e1-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="fe4e1-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fe4e1-113">GIF</span><span class="sxs-lookup"><span data-stu-id="fe4e1-113">'T</span></span>

<span data-ttu-id="fe4e1-114">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="fe4e1-114">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe4e1-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe4e1-115">See Also</span></span>

- [<span data-ttu-id="fe4e1-116">Microsoft. Quantum. Canon. applyumeachc</span><span class="sxs-lookup"><span data-stu-id="fe4e1-116">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="fe4e1-117">Microsoft. Quantum. Canon. applyumeacha</span><span class="sxs-lookup"><span data-stu-id="fe4e1-117">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="fe4e1-118">Microsoft. Quantum. Canon. applyumeachca</span><span class="sxs-lookup"><span data-stu-id="fe4e1-118">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)