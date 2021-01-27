---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Applytopartitionc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 43cf43fa2bf9c00a4096b39555b8f6080dd506d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850526"
---
# <a name="applytopartitionc-operation"></a><span data-ttu-id="14128-102">Applytopartitionc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="14128-102">ApplyToPartitionC operation</span></span>

<span data-ttu-id="14128-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="14128-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="14128-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="14128-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="14128-105">Wendet ein paar von Vorgängen auf eine bestimmte Partition eines Registers in zwei Teilen an.</span><span class="sxs-lookup"><span data-stu-id="14128-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="14128-106">Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="14128-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="14128-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14128-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-ctl"></a><span data-ttu-id="14128-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="14128-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="14128-109">Das auf die angegebene Partition anzuwendende paar von Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="14128-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="14128-110">numofqubitstofirstargument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="14128-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="14128-111">Anzahl der Qubits aus dem Ziel, die in den ersten Teil der Partition eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="14128-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="14128-112">Die restlichen Qubits bilden den zweiten Teil der Partition.</span><span class="sxs-lookup"><span data-stu-id="14128-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="14128-113">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="14128-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="14128-114">Ein Register von Qubits, die durch den angegebenen zwei Vorgang partitioniert und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="14128-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="14128-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="14128-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="14128-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14128-116">See Also</span></span>

- [<span data-ttu-id="14128-117">Microsoft. Quantum. Canon. applytopartition</span><span class="sxs-lookup"><span data-stu-id="14128-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)