---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA
title: Applydefirsttwoqubitsa-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 911e9bc3d02bf6c0395c30fa167a6cb730dc666e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704818"
---
# <a name="applytofirsttwoqubitsa-operation"></a><span data-ttu-id="057d9-102">Applydefirsttwoqubitsa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="057d9-102">ApplyToFirstTwoQubitsA operation</span></span>

<span data-ttu-id="057d9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="057d9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="057d9-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="057d9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="057d9-105">Wendet einen Vorgang auf die ersten beiden Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="057d9-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="057d9-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="057d9-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsA (op : ((Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="057d9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="057d9-107">Input</span></span>

### <a name="op--qubitqubit--unit-adj"></a><span data-ttu-id="057d9-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="057d9-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="057d9-109">Ein Vorgang, der auf die ersten beiden Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057d9-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="057d9-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="057d9-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="057d9-111">Qubit-Array zu den ersten zwei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="057d9-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="057d9-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="057d9-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="057d9-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="057d9-113">Remarks</span></span>

<span data-ttu-id="057d9-114">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="057d9-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="057d9-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="057d9-115">See Also</span></span>

- [<span data-ttu-id="057d9-116">Microsoft. Quantum. Canon. applyjefirsttwoqubits</span><span class="sxs-lookup"><span data-stu-id="057d9-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)