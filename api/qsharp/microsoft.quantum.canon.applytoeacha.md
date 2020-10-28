---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Applydeeacha-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 9485c6549ed4e1a6fb3abdfa3f85ba35579d8b0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704975"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="ce262-102">Applydeeacha-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ce262-102">ApplyToEachA operation</span></span>

<span data-ttu-id="ce262-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ce262-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ce262-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ce262-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ce262-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="ce262-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="ce262-106">Der-Modifizierer `A` gibt an, dass der Single-Qubit-Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="ce262-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="ce262-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce262-107">Input</span></span>

### <a name="singleelementoperation--t--unit-adj"></a><span data-ttu-id="ce262-108">singleelementoperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="ce262-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ce262-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ce262-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="ce262-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="ce262-110">register : 'T[]</span></span>

<span data-ttu-id="ce262-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce262-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ce262-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce262-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ce262-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ce262-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ce262-114">GIF</span><span class="sxs-lookup"><span data-stu-id="ce262-114">'T</span></span>

<span data-ttu-id="ce262-115">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="ce262-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce262-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ce262-116">See Also</span></span>

- [<span data-ttu-id="ce262-117">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="ce262-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)