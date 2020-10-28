---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Applydeeachc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: dfa18b6eb7a2c42fa2982994a2fc92170b52599c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704967"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="1f23a-102">Applydeeachc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1f23a-102">ApplyToEachC operation</span></span>

<span data-ttu-id="1f23a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1f23a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1f23a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1f23a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1f23a-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="1f23a-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="1f23a-106">Der-Modifizierer `C` gibt an, dass der Single-Qubit-Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="1f23a-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="1f23a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f23a-107">Input</span></span>

### <a name="singleelementoperation--t--unit-ctl"></a><span data-ttu-id="1f23a-108">singleelementoperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="1f23a-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="1f23a-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1f23a-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="1f23a-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="1f23a-110">register : 'T[]</span></span>

<span data-ttu-id="1f23a-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f23a-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1f23a-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1f23a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1f23a-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1f23a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1f23a-114">GIF</span><span class="sxs-lookup"><span data-stu-id="1f23a-114">'T</span></span>

<span data-ttu-id="1f23a-115">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="1f23a-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f23a-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f23a-116">See Also</span></span>

- [<span data-ttu-id="1f23a-117">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="1f23a-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)