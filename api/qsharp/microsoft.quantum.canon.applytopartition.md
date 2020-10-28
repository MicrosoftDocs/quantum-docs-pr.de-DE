---
uid: Microsoft.Quantum.Canon.ApplyToPartition
title: Applytopartition-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartition
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts.
ms.openlocfilehash: c1f43e7936fc1c18fb665388e9892dc3b74cdd05
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704727"
---
# <a name="applytopartition-operation"></a><span data-ttu-id="353aa-102">Applytopartition-Vorgang</span><span class="sxs-lookup"><span data-stu-id="353aa-102">ApplyToPartition operation</span></span>

<span data-ttu-id="353aa-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="353aa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="353aa-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="353aa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="353aa-105">Wendet ein paar von Vorgängen auf eine bestimmte Partition eines Registers in zwei Teilen an.</span><span class="sxs-lookup"><span data-stu-id="353aa-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>

```qsharp
operation ApplyToPartition (op : ((Qubit[], Qubit[]) => Unit), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="353aa-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="353aa-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="353aa-107">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="353aa-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="353aa-108">Das auf die angegebene Partition anzuwendende paar von Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="353aa-108">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="353aa-109">numofqubitstofirstargument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="353aa-109">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="353aa-110">Anzahl der Qubits aus dem Ziel, die in den ersten Teil der Partition eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="353aa-110">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="353aa-111">Die restlichen Qubits bilden den zweiten Teil der Partition.</span><span class="sxs-lookup"><span data-stu-id="353aa-111">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="353aa-112">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="353aa-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="353aa-113">Ein Register von Qubits, die durch den angegebenen zwei Vorgang partitioniert und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="353aa-113">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="353aa-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="353aa-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="353aa-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="353aa-115">See Also</span></span>

- [<span data-ttu-id="353aa-116">Microsoft. Quantum. Canon. applytopartitiona</span><span class="sxs-lookup"><span data-stu-id="353aa-116">Microsoft.Quantum.Canon.ApplyToPartitionA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionA)
- [<span data-ttu-id="353aa-117">Microsoft. Quantum. Canon. applytopartitionc</span><span class="sxs-lookup"><span data-stu-id="353aa-117">Microsoft.Quantum.Canon.ApplyToPartitionC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionC)
- [<span data-ttu-id="353aa-118">Microsoft. Quantum. Canon. applytopartitionca</span><span class="sxs-lookup"><span data-stu-id="353aa-118">Microsoft.Quantum.Canon.ApplyToPartitionCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartitionCA)