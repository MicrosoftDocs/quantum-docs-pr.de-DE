---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerClusterOperatorPQTerm
title: _ApplyJordanWignerClusterOperatorPQTerm Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerClusterOperatorPQTerm
qsharp.summary: Applies time-evolution by a cluster operator PQ term described by a `GeneratorIndex`.
ms.openlocfilehash: 67ec6fcfec097a14b1e31f94ac82ecf15109ecf6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851735"
---
# <a name="_applyjordanwignerclusteroperatorpqterm-operation"></a><span data-ttu-id="b1034-102">_ApplyJordanWignerClusterOperatorPQTerm Vorgang</span><span class="sxs-lookup"><span data-stu-id="b1034-102">_ApplyJordanWignerClusterOperatorPQTerm operation</span></span>

<span data-ttu-id="b1034-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="b1034-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="b1034-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b1034-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="b1034-105">Wendet die Zeit Weiterentwicklung durch einen Cluster Operator PQ-Begriff an, der von einem beschrieben wird `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="b1034-105">Applies time-evolution by a cluster operator PQ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerClusterOperatorPQTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b1034-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b1034-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="b1034-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="b1034-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="b1034-108">`GeneratorIndex` , der den pq-Begriff eines Cluster Operators darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1034-108">`GeneratorIndex` representing a cluster operator PQ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="b1034-109">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b1034-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b1034-110">Dauer der Zeitentwicklung.</span><span class="sxs-lookup"><span data-stu-id="b1034-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="b1034-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b1034-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b1034-112">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="b1034-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b1034-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b1034-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

