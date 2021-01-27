---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Diskretephaseschätzungsiterations-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 03e2300dcc2d2cb42992e074833c8cd2530e898b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839973"
---
# <a name="discretephaseestimationiteration-operation"></a><span data-ttu-id="6d169-102">Diskretephaseschätzungsiterations-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6d169-102">DiscretePhaseEstimationIteration operation</span></span>

<span data-ttu-id="6d169-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="6d169-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="6d169-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6d169-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6d169-105">Führt eine einzelne Iteration eines iterativen (klassisch gesteuerten) Phasen Schätz Algorithmus mithilfe von ganzzahligen Kräften eines einheitlichen Oracle aus.</span><span class="sxs-lookup"><span data-stu-id="6d169-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.</span></span>

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6d169-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d169-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="6d169-107">Oracle: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="6d169-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="6d169-108">Der Vorgang, der für eine ganze Zahl und ein Register ausgeführt wird, sodass $U ^ m $ auf das angegebene Register angewendet wird, wobei $U $ die einheitliche ist, deren Phase geschätzt werden soll, und wobei $m $ die ganzzahlige Potenz ist, die dem Oracle zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6d169-108">Operation acting on an integer and a register, such that $U^m$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $m$ is the integer power given to the oracle</span></span>


### <a name="power--int"></a><span data-ttu-id="6d169-109">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6d169-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6d169-110">Gibt an, wie oft das angegebene einheitliche Oracle angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d169-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="6d169-111">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6d169-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6d169-112">Der Winkel, um den die Phase auf dem Qubit des-Steuer Elements vor dem Ausführen des Ziel Zustands invertieren soll.</span><span class="sxs-lookup"><span data-stu-id="6d169-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="6d169-113">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6d169-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6d169-114">Das Registrierungsstatus, auf das der angegebene einheitliche Oracle reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="6d169-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="6d169-115">controlqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6d169-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6d169-116">Ein zusätzliches Qubit, das verwendet wird, um die Anwendung des angegebenen Oracle zu steuern.</span><span class="sxs-lookup"><span data-stu-id="6d169-116">An auxiliary qubit used to control the application of the given oracle.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6d169-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6d169-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

