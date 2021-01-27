---
uid: Microsoft.Quantum.Canon.ApplyToPartition
title: Applytopartition-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartition
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts.
ms.openlocfilehash: a0dc3453e7501816132569869e858418d5f3f4e5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850539"
---
# <a name="applytopartition-operation"></a><span data-ttu-id="b5b4d-102">Applytopartition-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b5b4d-102">ApplyToPartition operation</span></span>

<span data-ttu-id="b5b4d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b5b4d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b5b4d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b5b4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b5b4d-105">Wendet ein paar von Vorgängen auf eine bestimmte Partition eines Registers in zwei Teilen an.</span><span class="sxs-lookup"><span data-stu-id="b5b4d-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>

```qsharp
operation ApplyToPartition (op : ((Qubit[], Qubit[]) => Unit), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b5b4d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5b4d-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="b5b4d-107">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b5b4d-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b5b4d-108">Das auf die angegebene Partition anzuwendende paar von Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="b5b4d-108">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="b5b4d-109">numofqubitstofirstargument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b5b4d-109">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b5b4d-110">Anzahl der Qubits aus dem Ziel, die in den ersten Teil der Partition eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b5b4d-110">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="b5b4d-111">Die restlichen Qubits bilden den zweiten Teil der Partition.</span><span class="sxs-lookup"><span data-stu-id="b5b4d-111">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b5b4d-112">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b5b4d-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b5b4d-113">Ein Register von Qubits, die durch den angegebenen zwei Vorgang partitioniert und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="b5b4d-113">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b5b4d-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b5b4d-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="b5b4d-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b5b4d-115">See Also</span></span>

- [<span data-ttu-id="b5b4d-116">Microsoft. Quantum. Canon. applytopartitiona</span><span class="sxs-lookup"><span data-stu-id="b5b4d-116">Microsoft.Quantum.Canon.ApplyToPartitionA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionA)
- [<span data-ttu-id="b5b4d-117">Microsoft. Quantum. Canon. applytopartitionc</span><span class="sxs-lookup"><span data-stu-id="b5b4d-117">Microsoft.Quantum.Canon.ApplyToPartitionC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionC)
- [<span data-ttu-id="b5b4d-118">Microsoft. Quantum. Canon. applytopartitionca</span><span class="sxs-lookup"><span data-stu-id="b5b4d-118">Microsoft.Quantum.Canon.ApplyToPartitionCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionCA)