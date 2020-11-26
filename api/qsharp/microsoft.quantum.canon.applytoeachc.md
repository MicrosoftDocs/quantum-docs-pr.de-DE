---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Applydeeachc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 535f815503e20b5cee35f3f273a714203a4baf12
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217780"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="5f87c-102">Applydeeachc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5f87c-102">ApplyToEachC operation</span></span>

<span data-ttu-id="5f87c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5f87c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5f87c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5f87c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5f87c-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="5f87c-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="5f87c-106">Der-Modifizierer `C` gibt an, dass der Single-Qubit-Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="5f87c-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="5f87c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f87c-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-ctl"></a><span data-ttu-id="5f87c-108">singleelementoperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="5f87c-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="5f87c-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="5f87c-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="5f87c-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="5f87c-110">register : 'T[]</span></span>

<span data-ttu-id="5f87c-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f87c-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5f87c-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5f87c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5f87c-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="5f87c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5f87c-114">GIF</span><span class="sxs-lookup"><span data-stu-id="5f87c-114">'T</span></span>

<span data-ttu-id="5f87c-115">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="5f87c-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f87c-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5f87c-116">See Also</span></span>

- [<span data-ttu-id="5f87c-117">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="5f87c-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)