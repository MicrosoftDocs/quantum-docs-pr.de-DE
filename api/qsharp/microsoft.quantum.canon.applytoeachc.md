---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Applydeeachc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: b8b51e1c8d52c140c3ca1e5a54d0bd4cf4873046
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850857"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="f08f1-102">Applydeeachc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f08f1-102">ApplyToEachC operation</span></span>

<span data-ttu-id="f08f1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f08f1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f08f1-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f08f1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f08f1-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="f08f1-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="f08f1-106">Der-Modifizierer `C` gibt an, dass der Single-Qubit-Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="f08f1-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="f08f1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f08f1-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-ctl"></a><span data-ttu-id="f08f1-108">singleelementoperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="f08f1-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="f08f1-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f08f1-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="f08f1-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="f08f1-110">register : 'T[]</span></span>

<span data-ttu-id="f08f1-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f08f1-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f08f1-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f08f1-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f08f1-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f08f1-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f08f1-114">GIF</span><span class="sxs-lookup"><span data-stu-id="f08f1-114">'T</span></span>

<span data-ttu-id="f08f1-115">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="f08f1-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="f08f1-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f08f1-116">Example</span></span>

<span data-ttu-id="f08f1-117">Bereiten Sie einen "3-Qubit $ \ket{+} $"-Status vor:</span><span class="sxs-lookup"><span data-stu-id="f08f1-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="f08f1-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f08f1-118">See Also</span></span>

- [<span data-ttu-id="f08f1-119">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="f08f1-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)