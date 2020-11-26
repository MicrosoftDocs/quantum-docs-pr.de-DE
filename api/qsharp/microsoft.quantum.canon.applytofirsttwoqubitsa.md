---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA
title: Applydefirsttwoqubitsa-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 1a286c167a87372dc89d62ab3733b186298c43a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208702"
---
# <a name="applytofirsttwoqubitsa-operation"></a><span data-ttu-id="e8e38-102">Applydefirsttwoqubitsa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e8e38-102">ApplyToFirstTwoQubitsA operation</span></span>

<span data-ttu-id="e8e38-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8e38-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8e38-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8e38-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8e38-105">Wendet einen Vorgang auf die ersten beiden Qubits im Register an.</span><span class="sxs-lookup"><span data-stu-id="e8e38-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="e8e38-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="e8e38-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsA (op : ((Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="e8e38-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8e38-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-adj"></a><span data-ttu-id="e8e38-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="e8e38-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e8e38-109">Ein Vorgang, der auf die ersten beiden Qubits angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8e38-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="e8e38-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e8e38-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e8e38-111">Qubit-Array zu den ersten zwei Qubits, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8e38-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8e38-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8e38-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e8e38-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8e38-113">Remarks</span></span>

<span data-ttu-id="e8e38-114">Das entspricht:</span><span class="sxs-lookup"><span data-stu-id="e8e38-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="e8e38-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8e38-115">See Also</span></span>

- [<span data-ttu-id="e8e38-116">Microsoft. Quantum. Canon. applyjefirsttwoqubits</span><span class="sxs-lookup"><span data-stu-id="e8e38-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)