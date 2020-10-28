---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Continuousphaseschätzationiteration-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: a3914a4b19e3b898b6de8808699da09d386f487a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703656"
---
# <a name="continuousphaseestimationiteration-operation"></a><span data-ttu-id="014ab-102">Continuousphaseschätzationiteration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="014ab-102">ContinuousPhaseEstimationIteration operation</span></span>

<span data-ttu-id="014ab-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="014ab-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="014ab-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="014ab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="014ab-105">Führt eine einzelne Iteration eines iterativen (klassisch kontrollierten) Phasen Schätz Algorithmus mit beliebigen echten Kräften eines einheitlichen Oracle aus.</span><span class="sxs-lookup"><span data-stu-id="014ab-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.</span></span>

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="014ab-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="014ab-106">Input</span></span>

### <a name="oracle--continuousoracle"></a><span data-ttu-id="014ab-107">Oracle: [continuousoracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="014ab-107">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="014ab-108">Ein Vorgang, der auf einem Double-$t $ und einem Register ausgeführt wird, sodass $U ^ t $ auf das angegebene Register angewendet wird, wobei $U $ die einheitliche ist, deren Phase geschätzt werden soll, und wobei $t $ die ganzzahlige Potenz ist, die dem Oracle zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="014ab-108">Operation acting on a double $t$ and a register, such that $U^t$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $t$ is the integer power given to the oracle</span></span>


### <a name="time--double"></a><span data-ttu-id="014ab-109">Zeit: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="014ab-109">time : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="014ab-110">Gibt an, wie oft das angegebene einheitliche Oracle angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="014ab-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="014ab-111">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="014ab-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="014ab-112">Der Winkel, um den die Phase auf dem Qubit des-Steuer Elements vor dem Ausführen des Ziel Zustands invertieren soll.</span><span class="sxs-lookup"><span data-stu-id="014ab-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="014ab-113">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="014ab-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="014ab-114">Das Registrierungsstatus, auf das der angegebene einheitliche Oracle reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="014ab-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="014ab-115">controlqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="014ab-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="014ab-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="014ab-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

