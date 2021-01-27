---
uid: Microsoft.Quantum.Canon.ApplyToPartitionCA
title: Applytopartitionca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionCA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 572cf824647b3e7f7c0e17c797d519f41914f79d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841282"
---
# <a name="applytopartitionca-operation"></a><span data-ttu-id="eea18-102">Applytopartitionca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eea18-102">ApplyToPartitionCA operation</span></span>

<span data-ttu-id="eea18-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="eea18-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="eea18-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eea18-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eea18-105">Wendet ein paar von Vorgängen auf eine bestimmte Partition eines Registers in zwei Teilen an.</span><span class="sxs-lookup"><span data-stu-id="eea18-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="eea18-106">Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="eea18-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToPartitionCA (op : ((Qubit[], Qubit[]) => Unit is Ctl + Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="eea18-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="eea18-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="eea18-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="eea18-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="eea18-109">Das auf die angegebene Partition anzuwendende paar von Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="eea18-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="eea18-110">numofqubitstofirstargument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eea18-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eea18-111">Anzahl der Qubits aus dem Ziel, die in den ersten Teil der Partition eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eea18-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="eea18-112">Die restlichen Qubits bilden den zweiten Teil der Partition.</span><span class="sxs-lookup"><span data-stu-id="eea18-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="eea18-113">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="eea18-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="eea18-114">Ein Register von Qubits, die durch den angegebenen zwei Vorgang partitioniert und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="eea18-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eea18-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eea18-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="eea18-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eea18-116">See Also</span></span>

- [<span data-ttu-id="eea18-117">Microsoft. Quantum. Canon. applytopartition</span><span class="sxs-lookup"><span data-stu-id="eea18-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)