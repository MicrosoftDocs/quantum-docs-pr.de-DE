---
uid: Microsoft.Quantum.Canon.ApplyToPartitionA
title: Applytopartitiona-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: f8f773e9fc3c18467185f9717a235649be8b385a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841303"
---
# <a name="applytopartitiona-operation"></a><span data-ttu-id="8b59b-102">Applytopartitiona-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8b59b-102">ApplyToPartitionA operation</span></span>

<span data-ttu-id="8b59b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8b59b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8b59b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8b59b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8b59b-105">Wendet ein paar von Vorgängen auf eine bestimmte Partition eines Registers in zwei Teilen an.</span><span class="sxs-lookup"><span data-stu-id="8b59b-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="8b59b-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="8b59b-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToPartitionA (op : ((Qubit[], Qubit[]) => Unit is Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="8b59b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b59b-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-adj"></a><span data-ttu-id="8b59b-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="8b59b-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="8b59b-109">Das auf die angegebene Partition anzuwendende paar von Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="8b59b-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="8b59b-110">numofqubitstofirstargument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8b59b-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8b59b-111">Anzahl der Qubits aus dem Ziel, die in den ersten Teil der Partition eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b59b-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="8b59b-112">Die restlichen Qubits bilden den zweiten Teil der Partition.</span><span class="sxs-lookup"><span data-stu-id="8b59b-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="8b59b-113">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8b59b-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8b59b-114">Ein Register von Qubits, die durch den angegebenen zwei Vorgang partitioniert und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8b59b-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8b59b-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8b59b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="8b59b-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8b59b-116">See Also</span></span>

- [<span data-ttu-id="8b59b-117">Microsoft. Quantum. Canon. applytopartition</span><span class="sxs-lookup"><span data-stu-id="8b59b-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)