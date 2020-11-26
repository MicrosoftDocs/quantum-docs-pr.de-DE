---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: "\"Mess restabilizergenerators\"-Vorgang"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: 6c048c17df21d1026dc671f30d72a13ed8d8b7f5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200627"
---
# <a name="measurestabilizergenerators-operation"></a><span data-ttu-id="dc05b-102">"Mess restabilizergenerators"-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dc05b-102">MeasureStabilizerGenerators operation</span></span>

<span data-ttu-id="dc05b-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="dc05b-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="dc05b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dc05b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dc05b-105">Misst den angegebenen Satz von Generatoren einer stabilistabilisgruppe.</span><span class="sxs-lookup"><span data-stu-id="dc05b-105">Measures the given set of generators of a stabilizer group.</span></span>

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a><span data-ttu-id="dc05b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dc05b-106">Input</span></span>

### <a name="stabilizergroup--pauli"></a><span data-ttu-id="dc05b-107">stabilizergroup: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="dc05b-107">stabilizerGroup : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="dc05b-108">Ein Array von multiqubit-Pauli-Operatoren.</span><span class="sxs-lookup"><span data-stu-id="dc05b-108">An array of multiqubit Pauli operators.</span></span>
<span data-ttu-id="dc05b-109">Beispielsweise `stabilizerGroup[0]` ist eine Liste von Single-Qubit-Pauli-Matrizen, das tensorflow-Produkt, von dem ein stabiliatorgenerator ist.</span><span class="sxs-lookup"><span data-stu-id="dc05b-109">For example, `stabilizerGroup[0]` is a list of single-qubit Pauli matrices, the tensor product of which is a stabilizer generator.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="dc05b-110">logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="dc05b-110">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="dc05b-111">Ein Array von Qubits, in denen der stabilikocodecode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="dc05b-111">An array of qubits where the stabilizer code is defined.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="dc05b-112">Gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="dc05b-112">gadget : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="dc05b-113">Ein Vorgang, der angibt, wie ein multiqubit-Pauli-Operator gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc05b-113">An operation that specifies how to measure a multiqubit Pauli operator.</span></span>



## <a name="output--syndrome"></a><span data-ttu-id="dc05b-114">Ausgabe:- [Syndrom](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="dc05b-114">Output : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="dc05b-115">Das Ergebnis der Messungen.</span><span class="sxs-lookup"><span data-stu-id="dc05b-115">The result of measurements.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc05b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc05b-116">Remarks</span></span>

<span data-ttu-id="dc05b-117">Hiermit wird nicht überprüft, ob der angegebene Satz von Generatoren in den einzelnen Generatoren Überlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="dc05b-117">This does not check if the given set of generators are commuting.</span></span>
<span data-ttu-id="dc05b-118">Wenn keine Überprüfung durchzuführen ist, kann das Ergebnis von Messungen beliebig sein.</span><span class="sxs-lookup"><span data-stu-id="dc05b-118">If they are not commuting, the result of measurements may be arbitrary.</span></span>