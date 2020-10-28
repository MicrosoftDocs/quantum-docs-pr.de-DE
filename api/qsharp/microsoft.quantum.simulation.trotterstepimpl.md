---
uid: Microsoft.Quantum.Simulation.TrotterStepImpl
title: Trotterstepimpl-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStepImpl
qsharp.summary: Implements time-evolution by a term contained in a `GeneratorSystem`.
ms.openlocfilehash: 1ddd7ab33df243d729b5b48cba393d976bfd3640
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725327"
---
# <a name="trotterstepimpl-operation"></a><span data-ttu-id="6aeed-102">Trotterstepimpl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6aeed-102">TrotterStepImpl operation</span></span>

<span data-ttu-id="6aeed-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="6aeed-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="6aeed-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6aeed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6aeed-105">Implementiert die Zeitentwicklung mit einem in einem enthaltenen Begriff `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="6aeed-105">Implements time-evolution by a term contained in a `GeneratorSystem`.</span></span>

```qsharp
operation TrotterStepImpl (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, idx : Int, stepsize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="6aeed-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6aeed-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="6aeed-107">evolutiongenerator: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="6aeed-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="6aeed-108">Eine umfassende Beschreibung des Systems, das simuliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6aeed-108">A complete description of the system to be simulated.</span></span>


### <a name="idx--int"></a><span data-ttu-id="6aeed-109">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6aeed-109">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6aeed-110">Ganzzahliger Index zu einem Begriff im beschriebenen System.</span><span class="sxs-lookup"><span data-stu-id="6aeed-110">Integer index to a term in the described system.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="6aeed-111">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6aeed-111">stepsize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6aeed-112">Multiplikator für die Dauer der Zeit-Evolution nach Begriff, indiziert von `idx` .</span><span class="sxs-lookup"><span data-stu-id="6aeed-112">Multiplier on duration of time-evolution by term indexed by `idx`.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="6aeed-113">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6aeed-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6aeed-114">Die von der Simulation abgewickelten Qubits.</span><span class="sxs-lookup"><span data-stu-id="6aeed-114">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6aeed-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6aeed-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

