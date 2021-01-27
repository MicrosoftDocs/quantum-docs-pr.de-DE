---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Continuousphaseschätzationiteration-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: 925b9040f6d9cda074b18a6f9079ccb653f9fa98
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851906"
---
# <a name="continuousphaseestimationiteration-operation"></a><span data-ttu-id="77e80-102">Continuousphaseschätzationiteration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77e80-102">ContinuousPhaseEstimationIteration operation</span></span>

<span data-ttu-id="77e80-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="77e80-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="77e80-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="77e80-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="77e80-105">Führt eine einzelne Iteration eines iterativen (klassisch kontrollierten) Phasen Schätz Algorithmus mit beliebigen echten Kräften eines einheitlichen Oracle aus.</span><span class="sxs-lookup"><span data-stu-id="77e80-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.</span></span>

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="77e80-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77e80-106">Input</span></span>

### <a name="oracle--continuousoracle"></a><span data-ttu-id="77e80-107">Oracle: [continuousoracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="77e80-107">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="77e80-108">Ein Vorgang, der auf einem Double-$t $ und einem Register ausgeführt wird, sodass $U ^ t $ auf das angegebene Register angewendet wird, wobei $U $ die einheitliche ist, deren Phase geschätzt werden soll, und wobei $t $ die ganzzahlige Potenz ist, die dem Oracle zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="77e80-108">Operation acting on a double $t$ and a register, such that $U^t$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $t$ is the integer power given to the oracle</span></span>


### <a name="time--double"></a><span data-ttu-id="77e80-109">Zeit: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="77e80-109">time : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="77e80-110">Gibt an, wie oft das angegebene einheitliche Oracle angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="77e80-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="77e80-111">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="77e80-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="77e80-112">Der Winkel, um den die Phase auf dem Qubit des-Steuer Elements vor dem Ausführen des Ziel Zustands invertieren soll.</span><span class="sxs-lookup"><span data-stu-id="77e80-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="77e80-113">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="77e80-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="77e80-114">Das Registrierungsstatus, auf das der angegebene einheitliche Oracle reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="77e80-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="77e80-115">controlqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="77e80-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="77e80-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77e80-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

