---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerClusterOperatorPQRSTerm
title: _ApplyJordanWignerClusterOperatorPQRSTerm Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerClusterOperatorPQRSTerm
qsharp.summary: Applies time-evolution by a cluster operator PQRS term described by a `GeneratorIndex`.
ms.openlocfilehash: 5e43f81714128629a63befccb31092adbe9c9e82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204044"
---
# <a name="_applyjordanwignerclusteroperatorpqrsterm-operation"></a><span data-ttu-id="f445f-102">_ApplyJordanWignerClusterOperatorPQRSTerm Vorgang</span><span class="sxs-lookup"><span data-stu-id="f445f-102">_ApplyJordanWignerClusterOperatorPQRSTerm operation</span></span>

<span data-ttu-id="f445f-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="f445f-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="f445f-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f445f-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="f445f-105">Wendet die Zeit Weiterentwicklung durch einen von einem beschriebenen pqrs-Begriff eines Cluster Operators an `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="f445f-105">Applies time-evolution by a cluster operator PQRS term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerClusterOperatorPQRSTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f445f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f445f-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="f445f-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="f445f-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="f445f-108">`GeneratorIndex` , der den pqrs-Begriff eines Cluster Operators darstellt.</span><span class="sxs-lookup"><span data-stu-id="f445f-108">`GeneratorIndex` representing a cluster operator PQRS term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="f445f-109">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f445f-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f445f-110">Dauer der Zeitentwicklung.</span><span class="sxs-lookup"><span data-stu-id="f445f-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="f445f-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f445f-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f445f-112">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="f445f-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f445f-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f445f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

