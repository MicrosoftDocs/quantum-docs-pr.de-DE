---
uid: Microsoft.Quantum.Simulation.EstimateEnergyWithAdiabaticEvolution
title: Estimateenergywithadiabaticevolution-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergyWithAdiabaticEvolution
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: 3fdbdd83b784cdc560e3160151fdf4ba4e7115e6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722065"
---
# <a name="estimateenergywithadiabaticevolution-operation"></a><span data-ttu-id="5292a-102">Estimateenergywithadiabaticevolution-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5292a-102">EstimateEnergyWithAdiabaticEvolution operation</span></span>

<span data-ttu-id="5292a-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5292a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5292a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5292a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5292a-105">Führt die Zustands Vorbereitung durch Anwenden eines `statePrepUnitary` auf einen automatisch zugeordneten Eingabe Zustand, gefolgt von der adiabatischen Zustands Vorbereitung mithilfe eines `adiabaticUnitary` und schließlich der Phasen Schätzung in Bezug auf `qpeUnitary` den resultierenden Zustand mithilfe von aus `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="5292a-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergyWithAdiabaticEvolution (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="5292a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5292a-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="5292a-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5292a-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5292a-108">Anzahl von Qubits, die für die Simulation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5292a-108">Number of qubits used for the simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="5292a-109">stateprepeinheitlicher: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5292a-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5292a-110">Ein Oracle, das die Zustands Vorbereitung für den ursprünglichen Dynamical-Generator darstellt.</span><span class="sxs-lookup"><span data-stu-id="5292a-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="adiabaticunitary--qubit--unit"></a><span data-ttu-id="5292a-111">adiabaticeinheitlicher: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5292a-111">adiabaticUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5292a-112">Ein Oracle, das den Adiabatic Evolution-Algorithmus darstellt, der verwendet wird, um die Sweep-bis zum Endzustand des Algorithmus zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5292a-112">An oracle representing the adiabatic evolution algorithm to be used to implement the sweeps to the final state of the algorithm.</span></span>


### <a name="qpeunitary--qubit--unit-adj--ctl"></a><span data-ttu-id="5292a-113">qpeer einheitlich: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="5292a-113">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="5292a-114">Ein Oracle, das einen einheitlichen Operator $U $ darstellt, der die Entwicklung für "Time $ \delta t $" unter einem Dynamical Generator mit dem "Ground State $ \ket{\phi} $" und "Ground State Energy $E = \phi \\ , \delta t $" darstellt.</span><span class="sxs-lookup"><span data-stu-id="5292a-114">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="5292a-115">phaseestalgorithmus: ([diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5292a-115">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="5292a-116">Ein Vorgang, der die Phasen Schätzung für einen angegebenen einheitlichen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="5292a-116">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="5292a-117">Weitere Informationen finden Sie unter [iterative Phasen Schätzung](/quantum/libraries/characterization#iterative-phase-estimation) .</span><span class="sxs-lookup"><span data-stu-id="5292a-117">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="5292a-118">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5292a-118">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5292a-119">Eine Schätzung von $ \hat{\phi} $ der Erde State Energy $ \phi $ des durch $U $ dargestellten Generators.</span><span class="sxs-lookup"><span data-stu-id="5292a-119">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the generator represented by $U$.</span></span>