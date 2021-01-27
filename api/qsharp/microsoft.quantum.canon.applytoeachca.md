---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Applydeeachca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: c85b33760eba8d10d9650be2f8306e4afdd1f307
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841486"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="9a16c-102">Applydeeachca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9a16c-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="9a16c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9a16c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9a16c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9a16c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9a16c-105">Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="9a16c-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="9a16c-106">Der-Modifizierer `CA` gibt an, dass der Single-Qubit-Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="9a16c-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9a16c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a16c-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a><span data-ttu-id="9a16c-108">singleelementoperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="9a16c-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="9a16c-109">Der auf die einzelnen Qubits anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9a16c-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="9a16c-110">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="9a16c-110">register : 'T[]</span></span>

<span data-ttu-id="9a16c-111">Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a16c-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9a16c-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a16c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9a16c-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9a16c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9a16c-114">GIF</span><span class="sxs-lookup"><span data-stu-id="9a16c-114">'T</span></span>

<span data-ttu-id="9a16c-115">Das Ziel, für das der Vorgang fungiert.</span><span class="sxs-lookup"><span data-stu-id="9a16c-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="9a16c-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9a16c-116">Example</span></span>

<span data-ttu-id="9a16c-117">Bereiten Sie einen "3-Qubit $ \ket{+} $"-Status vor:</span><span class="sxs-lookup"><span data-stu-id="9a16c-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="9a16c-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a16c-118">See Also</span></span>

- [<span data-ttu-id="9a16c-119">Microsoft. Quantum. Canon. applyyeach</span><span class="sxs-lookup"><span data-stu-id="9a16c-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)