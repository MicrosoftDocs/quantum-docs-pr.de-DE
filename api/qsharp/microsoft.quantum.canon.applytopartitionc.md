---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Applytopartitionc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 840c93c653d71af1a82fb0dc51d9e056176ba88b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704711"
---
# <a name="applytopartitionc-operation"></a><span data-ttu-id="9c7ef-102">Applytopartitionc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9c7ef-102">ApplyToPartitionC operation</span></span>

<span data-ttu-id="9c7ef-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9c7ef-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9c7ef-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9c7ef-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9c7ef-105">Wendet ein paar von Vorgängen auf eine bestimmte Partition eines Registers in zwei Teilen an.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-105">Applies a pair of operations to a given partition of a register into two parts.</span></span>
<span data-ttu-id="9c7ef-106">Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="9c7ef-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9c7ef-107">Input</span></span>

### <a name="op--qubitqubit--unit-ctl"></a><span data-ttu-id="9c7ef-108">OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="9c7ef-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9c7ef-109">Das auf die angegebene Partition anzuwendende paar von Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-109">The pair of operations to be applied to the given partition.</span></span>


### <a name="numberofqubitstofirstargument--int"></a><span data-ttu-id="9c7ef-110">numofqubitstofirstargument: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9c7ef-110">numberOfQubitsToFirstArgument : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9c7ef-111">Anzahl der Qubits aus dem Ziel, die in den ersten Teil der Partition eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-111">Number of qubits from target to put into the first part of the partition.</span></span>
<span data-ttu-id="9c7ef-112">Die restlichen Qubits bilden den zweiten Teil der Partition.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-112">The remaining qubits constitute the second part of the partition.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9c7ef-113">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9c7ef-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9c7ef-114">Ein Register von Qubits, die durch den angegebenen zwei Vorgang partitioniert und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-114">A register of qubits that are being partitioned and operated on by the given two operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9c7ef-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9c7ef-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="9c7ef-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9c7ef-116">See Also</span></span>

- [<span data-ttu-id="9c7ef-117">Microsoft. Quantum. Canon. applytopartition</span><span class="sxs-lookup"><span data-stu-id="9c7ef-117">Microsoft.Quantum.Canon.ApplyToPartition</span></span>](xref:Microsoft.Quantum.Canon.ApplyToPartition)